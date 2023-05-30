<!DOCTYPE html>
<html>
<head>
  <style>
    .playlist-item {
      margin-bottom: 10px;
    }
  </style>
</head>
<body>
  <div id="playlist"></div>

  <h2>Add a new song</h2>
  <form id="songForm">
    <label for="title">Title:</label><br>
    <input type="text" id="title" name="title"><br>
    <label for="artist">Artist:</label><br>
    <input type="text" id="artist" name="artist"><br>
    <label for="duration">Duration:</label><br>
    <input type="number" id="duration" name="duration"><br>
    <input type="submit" value="Add Song">
  </form>

  <button onclick="displaySongs(sortByTitle())">Sort by Title</button>
  <button onclick="displaySongs(sortByArtist())">Sort by Artist</button>
  <button onclick="displaySongs(sortByDuration())">Sort by Duration</button>

  <script>
    let playlist = [
      { id: 1, title: 'Song 1', artist: 'Artist 1', duration: 180 },
      { id: 2, title: 'Song 2', artist: 'Artist 2', duration: 240 },
    ];

    // CRUD functions
    function addSong(song) {
      playlist.push(song);
    }

    function sortByTitle() {
      return playlist.sort((a, b) => a.title.localeCompare(b.title));
    }

    function sortByArtist() {
      return playlist.sort((a, b) => a.artist.localeCompare(b.artist));
    }

    function sortByDuration() {
      return playlist.sort((a, b) => a.duration - b.duration);
    }

    function displaySongs(playlist) {
      const playlistDiv = document.getElementById('playlist');
      playlistDiv.innerHTML = '';
      playlist.forEach(song => {
        const songDiv = document.createElement('div');
        songDiv.classList.add('playlist-item');
        songDiv.textContent = `${song.title} by ${song.artist}, Duration: ${song.duration}s`;
        playlistDiv.appendChild(songDiv);
      });
    }

    document.getElementById('songForm').addEventListener('submit', function(event) {
      event.preventDefault();
      const title = document.getElementById('title').value;
      const artist = document.getElementById('artist').value;
      const duration = Number(document.getElementById('duration').value);
      const id = playlist.length + 1; // simple way to generate unique IDs
      addSong({ id, title, artist, duration });
      displaySongs(playlist);
    });

    // Display the initial playlist
    displaySongs(playlist);
  </script>
</body>
</html>
