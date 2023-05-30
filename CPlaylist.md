<html lang="en">
<head>
    <title>Playlist Management</title>
</head>
<body>
    <h1>Playlist Management</h1>
    <i>Enter the name of a playlist to get started</i>
    <input placeholder="Playlist" id="play" />
    <p>If you already have a saved playlist, enter its name above and hit "load playlist"</p>
    <button onclick="loadPlaylists()">Load Playlist</button>
    <table class="teams" border="1">
        <tr>
            <th>ID</th>
            <th>Playlist</th>
            <th>Duration</th>
            <th>Year</th>
            <th id="ageHeader" onclick="sortTableByAge()">Age</th>
            <th>Rating</th>
            <th>Artist</th>
            <th>Title</th>
        </tr>
    </table>
    <hr />
    <div id="existingPlaylists">
    </div>
    <div id="playlistBox">
        <div>
            <h2>Add playlist</h2>
            <form id="aplaylist">
                <input required placeholder="Playlist" id="playlist_name" />
                <input required placeholder="Duration" id="duration" />
                <input required placeholder="Title" id="title" />
                <input required placeholder="Year" id="year" />
                <input required placeholder="Age" id="age" />
                <input required placeholder="Rating" id="rating" />
                <textarea required placeholder="Artist" id="artist"></textarea>
                <button type="submit" onclick="addPlaylist()">Add Playlist</button>
            </form>
        </div>
    </div>

    <script>
        let playlistLoader = {};
        let currentPlaylist = -1;
        // change in AWS
        const url = "";

        const previewPlaylist = (playlist) => {
            document.getElementById("PlaylistName").innerHTML = "Playlist Name: " + playlist.playlist_name;
            document.getElementById("Duration").innerHTML = "Duration: " + playlist.duration;
            document.getElementById("Year").innerHTML = "Year: " + playlist.year;
            document.getElementById("Age").innerHTML = "Age: " + playlist.age;
            document.getElementById("Rating").innerHTML = "Rating: " + playlist.rating + " stars";
            document.getElementById("Artist").innerHTML = "Artist:\n" + playlist.artist;
            currentPlaylist = playlist.id;
        };

        const addPlaylist = () => {
            const playlist_name = document.getElementById("playlist_name").value;
            const duration = document.getElementById("duration").value;
            const title = document.getElementById("title").value;
            const year = document.getElementById("year").value;
            const age = document.getElementById("age").value;
            const rating = document.getElementById("rating").value;
            const artist = document.getElementById("artist").value;

            if (play === "") {
                alert("Invalid playlist!");
                return;
            }
            data = {
                playlist_name: playlist_name,
                duration: duration,
                title: title,
                year: year,
                age: age,
                rating: rating,
                artist: artist,
            };
            var requestOptions = {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify(data),
            };
            try {
                fetch(`http://localhost:8086/playlist`, requestOptions)
                    .then(response => response.json())
                    .then(data => {
                        console.log("Success");
                        alert("Added Playlist");
                    })
                    .catch(error => console.error(error));
            } catch (e) {
                console.log(e);
            }
        };

        const loadPlaylists = () => {
            const teams = document.querySelector(".teams");
            var rowCount = teams.rows.length;
            for (var i = rowCount - 1; i >= 1; i--) {
                teams.deleteRow(i);
            }
            const play = document.getElementById("play").value;
            if (play === "") {
                alert("Invalid playlist!");
                return;
            }
            try {
                fetch(`http://localhost:8086/playlist?playlist_name=` + play)
                    .then(response => response.json())
                    .then(data => {
                        if (data.length > 0) {
                            data.forEach((data) => {
                                teams.innerHTML += `
                                    <tr>
                                        <td>${data.id}</td>
                                        <td>${data.playlist_name}</td>
                                        <td>${data.duration}</td>
                                        <td>${data.year}</td>
                                        <td>${data.age}</td>
                                        <td>${data.rating}</td>
                                        <td>${data.artist}</td>
                                        <td>${data.title}</td>
                                    </tr>`;
                            });
                        } else {
                            alert("Invalid Name");
                        }
                    })
                    .catch(error => console.error(error));
            } catch (e) {
                console.log(e);
            }
        };

        const deletePlaylist = () => {
            if (currentPlaylist < 0) {
                alert("Invalid playlist!");
                return;
            }

            fetch(url, {
                method: 'DELETE',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({ id: currentPlaylist }),
            }).then(() => {
                alert("Success, deleted!");
                loadPlaylists();
            });
        };

        const sortTableByAge = () => {
            const table = document.querySelector(".teams");
            const rows = Array.from(table.rows);

            // Remove the current sorting indicator
            const previousSortIndicator = document.querySelector(".sort-indicator");
            if (previousSortIndicator) {
                previousSortIndicator.parentNode.removeChild(previousSortIndicator);
            }

            // Get the index of the "Age" column
            const ageColumnIndex = Array.from(table.rows[0].cells).findIndex(cell => cell.id === "ageHeader");

            // Sort the rows based on the age values
            rows.sort((a, b) => {
                const ageA = parseInt(a.cells[ageColumnIndex].innerText);
                const ageB = parseInt(b.cells[ageColumnIndex].innerText);
                return ageA - ageB;
            });

            // Rebuild the table with sorted rows
            const tbody = table.querySelector("tbody");
            rows.forEach(row => tbody.appendChild(row));

            // Add sorting indicator
            const ageHeaderCell = document.getElementById("ageHeader");
            ageHeaderCell.innerHTML += '<span class="sort-indicator">&#x25B2;</span>';
        };

        const maybePlay = localStorage.getItem("play");
        if (maybePlay !== null) {
            document.getElementById("play").value = maybePlay;
            loadPlaylists();
        }
    </script>

    <style>
        input,
        textarea {
            display: block;
            width: 400px;

            background-color: white;
            outline: none;
            border: 1px solid brown;
            padding: 4px;
            margin: 6px 0px;
            font-size: 18px;
        }

        hr {
            margin-top: 20px;
        }

        #existingPlaylists {
            display: flex;
            gap: 15px;
            margin-bottom: 15px;
        }

        button {
            background-color: #ffcc00;
            outline: none;
            border: 1px solid #ffcc00;
            color: black;
            padding: 6px;
            font-size: 18px;
            transition: all 0.1s linear;
        }

        button:hover {
            background-color: #aa8800;
            border: 1px solid #aa8800;
            transform: translateY(-5px);
        }

        #playlistBox {
            display: flex;
            flex-direction: row;
            gap: 40px;
        }

        #previewPlaylist > p {
            margin: 4px 0px;
            font-size: 18px;
        }

        .sort-indicator {
            font-size: 12px;
            margin-left: 5px;
        }
    </style>
</body>
</html>
