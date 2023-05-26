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
    // Call the renderPlaylists function to populate the frontend with playlists
    renderPlaylists();
  </script>
</body>
</html>


<html>
<head>
    <title>Music Player Sorting</title>
    <style>
    body {
        font-family: Arial, sans-serif;
        background-color: #F5F5F5;
    }
    h1 {
        color: #5A5A5A;
    }
    #musicList {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;
    }
    .musicItem {
        display: flex;
        justify-content: space-between;
        align-items: center;
        border: 1px solid #ccc;
        padding: 10px;
        width: 300px;
        border-radius: 10px;
    }
    button {
        margin-top: 20px;
        padding: 10px 20px;
        border: none;
        background-color: #555;
        color: #fff;
        font-size: 16px;
        cursor: pointer;
        border-radius: 5px;
    }
    button:hover {
        background-color: #444;
    }
    </style>
</head>
<body>
    <h1>Music Player</h1>
    <div id="musicList">
        <!-- The list of songs will be inserted here -->
    </div>
    <button onclick="sortMusic()">Sort by duration</button>
    <script>
    var musicList = [
        {title: 'Mood', artist: 'Ian Dior', duration: 189},
        {title: 'Gone Girl', artist: 'Ian Dior', duration: 158},
        {title: 'Prospect', artist: 'Ian Dior', duration: 173},
        {title: '18', artist: 'Ian Dior', duration: 199},
        {title: 'Holding On', artist: 'Ian Dior', duration: 186},
    ];
    function sortMusic() {
        musicList.sort((a, b) => a.duration - b.duration);
        displayMusic();
    }
    function displayMusic() {
        var musicListDiv = document.getElementById('musicList');
        musicListDiv.innerHTML = '';
        for (var i = 0; i < musicList.length; i++) {
            var musicItemDiv = document.createElement('div');
            musicItemDiv.className = 'musicItem';
            musicItemDiv.innerHTML = `<span>${musicList[i].title} by ${musicList[i].artist}</span><span>${musicList[i].duration} seconds</span>`;
            musicListDiv.appendChild(musicItemDiv);
        }
    }
    // displayMusic();
    </script>
</body>
</html>