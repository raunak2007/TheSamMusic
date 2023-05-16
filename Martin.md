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
        name: 'Workout',
        genre: 'Pop',
        tracks: [
          { title: 'Believer', artist: 'Imagine Dragons' },
          { title: 'Thunder', artist: 'Imagine Dragons' },
          // Add more tracks as needed
        ]
      },
      {
        name: 'Chill Vibes',
        genre: 'Electronic',
        tracks: [
          { title: 'Summer', artist: 'Calvin Harris' },
          { title: 'Sunflower', artist: 'Post Malone & Swae Lee' },
          // Add more tracks as needed
        ]
      },
      {
        name: 'Party Mix',
        genre: 'Pop',
        tracks: [
          { title: 'Dance Monkey', artist: 'Tones and I' },
          { title: 'Blinding Lights', artist: 'The Weeknd' },
          // Add more tracks as needed
        ]
      },
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
    // Prompt to add a new playlist
    function addPlaylist() {
      const playlistName = prompt('Enter the playlist name:');
      const playlistGenre = prompt('Enter the playlist genre:');
      const playlist = {
        name: playlistName,
        genre: playlistGenre,
