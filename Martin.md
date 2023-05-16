<!DOCTYPE html>
<html>
<head>
  <title>Playlist Manager</title>
  <style>
    /* Add some basic styling */
    body {
      font-family: Arial, sans-serif;
    }
    
    h1 {
      text-align: center;
    }
    
    .playlist-form {
      text-align: center;
      margin-bottom: 20px;
    }
    
    .playlist-item {
      display: flex;
      align-items: center;
      margin-bottom: 10px;
    }
    
    .playlist-item input[type="text"] {
      flex: 1;
      margin-right: 10px;
    }
    
    .playlist-item button {
      margin-left: 10px;
    }
  </style>
</head>
<body>
  <h1>Playlist Manager</h1>
  
  <div class="playlist-form">
    <input type="text" id="playlist-input" placeholder="Enter playlist name">
    <button onclick="addPlaylist()">Add Playlist</button>
  </div>
  
  <div id="playlist-container"></div>

  <script>
    // Initialize an empty array to store the playlists
    let playlists = [];
    
    function addPlaylist() {
      // Get the playlist name from the input field
      const playlistInput = document.getElementById('playlist-input');
      const playlistName = playlistInput.value;
      
      // Create a new playlist object
      const playlist = { name: playlistName, songs: [] };
      
      // Add the new playlist to the array
      playlists.push(playlist);
      
      // Clear the input field
      playlistInput.value = '';
      
      // Refresh the playlist display
      displayPlaylists();
    }
    
    function displayPlaylists() {
      const playlistContainer = document.getElementById('playlist-container');
      
      // Clear the playlist container
      playlistContainer.innerHTML = '';
      
      // Loop through the playlists array and create HTML elements for each playlist
      playlists.forEach(function(playlist) {
        const playlistItem = document.createElement('div');
        playlistItem.classList.add('playlist-item');
        
        const playlistName = document.createElement('span');
        playlistName.textContent = playlist.name;
        
        const deleteButton = document.createElement('button');
        deleteButton.textContent = 'Delete';
        deleteButton.addEventListener('click', function() {
          deletePlaylist(playlist);
        });
        
        playlistItem.appendChild(playlistName);
        playlistItem.appendChild(deleteButton);
        
        playlistContainer.appendChild(playlistItem);
      });
    }
    
    function deletePlaylist(playlist) {
      // Find the index of the playlist in the array
      const index = playlists.indexOf(playlist);
      
      // Remove the playlist from the array
      playlists.splice(index, 1);
      
      // Refresh the playlist display
      displayPlaylists();
    }
  </script>
</body>
</html>
