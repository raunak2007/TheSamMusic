<!DOCTYPE html>
<html>
<head>
  <title>Music Playlist Manager</title>
  <style>
    /* CSS styles for the frontend interface */
    /* Add your own styles and customize as needed */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #333;
      color: #fff;
      padding: 10px;
      text-align: center;
    }
    .container {
      max-width: 800px;
      margin: 0 auto;
      padding: 20px;
    }
    .playlist-item {
      border: 1px solid #ccc;
      border-radius: 5px;
      padding: 10px;
      margin-bottom: 10px;
    }
    .playlist-item:hover {
      background-color: #F5F5F5;
    }
    .playlist-item h3 {
      margin-top: 0;
    }
    .playlist-item p {
      margin-bottom: 0;
    }
  </style>
</head>
<body>
  <header>
    <h1>Music Playlist Manager</h1>
  </header>
  <div class="container">
    <h2>My Playlists</h2>
    <div id="playlist-container"></div>
  </div>
  <script>
    // JavaScript code to interact with the backend and populate the playlists
    // Example playlist data
    const playlists = [
      {
        name: 'Workout Mix',
        genre: 'Pop',
        tracks: [
          { title: 'Track 1', artist: 'Artist 1' },
          { title: 'Track 2', artist: 'Artist 2' },
          // Add more tracks as needed
        ]
      },
      {
        name: 'Chill Vibes',
        genre: 'Electronic',
        tracks: [
          { title: 'Track 3', artist: 'Artist 3' },
          { title: 'Track 4', artist: 'Artist 4' },
          // Add more tracks as needed
        ]
      },
      // Add more playlists as needed
    ];
    // Function to render the playlists on the frontend
    function renderPlaylists() {
      const playlistContainer = document.getElementById('playlist-container');
      playlists.forEach(playlist => {
        const playlistItem = document.createElement('div');
        playlistItem.classList.add('playlist-item');
        const playlistTitle = document.createElement('h3');
        playlistTitle.textContent = playlist.name;
        const playlistGenre = document.createElement('p');
        playlistGenre.textContent = `Genre: ${playlist.genre}`;
        const playlistTracks = document.createElement('ul');
        playlist.tracks.forEach(track => {
          const trackItem = document.createElement('li');
          trackItem.textContent = `${track.title} - ${track.artist}`;
          playlistTracks.appendChild(trackItem);
        });
        playlistItem.appendChild(playlistTitle);
        playlistItem.appendChild(playlistGenre);
        playlistItem.appendChild(playlistTracks);
        playlistContainer.appendChild(playlistItem);
      });
    }
    // Call the renderPlaylists function to populate the frontend with playlists
    renderPlaylists();
  </script>
</body>
</html>
