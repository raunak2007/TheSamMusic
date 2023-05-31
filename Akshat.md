<html>
<head>
  <style>
    body {
      font-family: Arial, sans-serif;
       color: black;
    }
    .song-item {
      border: 1px solid #ccc;
      margin-bottom: 10px;
      padding: 10px;
      border-radius: 5px;
      background-color: #f9f9f9;
    }
    form {
      background-color: #f3f3f3;
      padding: 15px;
      margin-bottom: 20px;
      border-radius: 5px;
    }
    label {
      display: block;
      margin-bottom: 5px;
    }
    input[type="text"],
    input[type="number"],
    select {
      width: 100%;
      padding: 10px;
      margin-bottom: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    input[type="submit"] {
      background-color: #4CAF50;
      border: none;
      color: white;
      padding: 15px 32px;
      text-align: center;
      text-decoration: none;
      display: inline-block;
      font-size: 16px;
      border-radius: 5px;
      cursor: pointer;
    }
    button {
      background-color: #008CBA;
      border: none;
      color: white;
      padding: 10px;
      text-align: center;
      text-decoration: none;
      display: inline-block;
      font-size: 14px;
      margin: 4px 2px;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h2>Add favorites here!</h2>
  <form id="songForm">
    <label for="title">Title:</label>
    <input type="text" id="title" name="title">
    <label for="artist">Artist:</label>
    <input type="text" id="artist" name="artist">
    <label for="genre">Genre:</label>
    <input type="text" id="genre" name="genre">
    <label for="length">Length (minutes):</label>
    <input type="number" id="length" name="length">
    <input type="submit" value="Add Song">
  </form>

  <div id="songs"></div>

  <button onclick="sortAndSearch(sortByTitle)">Sort by Title</button>
  <button onclick="sortAndSearch(sortByArtist)">Sort by Artist</button>
  <button onclick="sortAndSearch(sortByGenre)">Sort by Genre</button>
  <button onclick="sortAndSearch(sortByLength)">Sort by Length</button>

  <script>
    let songs = JSON.parse(localStorage.getItem('songs')) || [];

    function addSong(song) {
      songs.push(song);
      localStorage.setItem('songs', JSON.stringify(songs));
    }

    function displaySongs(sortedSongs) {
      const songsDiv = document.getElementById('songs');
      songsDiv.innerHTML = '';
      sortedSongs.forEach(song => {
        const songDiv = document.createElement('div');
        songDiv.classList.add('song-item');
        songDiv.textContent = `${song.title} by ${song.artist}, Genre: ${song.genre}, Length: ${song.length} minutes`;
        songsDiv.appendChild(songDiv);
      });
    }

    function sortByTitle() {
      return [...songs].sort((a, b) => a.title.localeCompare(b.title));
    }

    function sortByArtist() {
      return [...songs].sort((a, b) => a.artist.localeCompare(b.artist));
    }

    function sortByGenre() {
      return [...songs].sort((a, b) => a.genre.localeCompare(b.genre));
    }

    function sortByLength() {
      return [...songs].sort((a, b) => a.length - b.length);
    }

    function sortAndSearch(sortFunction) {
      const searchText = prompt("Enter search text:");
      let sortedSongs = sortFunction();
      if (searchText !== null && searchText !== '') {
        sortedSongs = sortedSongs.filter(song => song.title.includes(searchText) || song.artist.includes(searchText) || song.genre.includes(searchText));
      }
      displaySongs(sortedSongs);
    }

    document.getElementById('songForm').addEventListener('submit', function(event) {
      event.preventDefault();
      const title = document.getElementById('title').value;
      const artist = document.getElementById('artist').value;
      const genre = document.getElementById('genre').value;
      const length = Number(document.getElementById('length').value);
      addSong({ title, artist, genre, length });
      displaySongs(songs);
    });

    // Display the initial songs
    displaySongs(songs);
  </script>
</body>
</html>
