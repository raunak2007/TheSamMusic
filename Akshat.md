<html>
<head>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #F0F0F0;
      color: black;
    }
    .song-item {
      border: 1px solid #ccc;
      margin-bottom: 10px;
      padding: 10px;
      border-radius: 5px;
      background-color: #fff;
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
  <h2>Add your favorites</h2>
  <form id="songForm">
    <label for="title">Title:</label>
    <input type="text" id="title" name="title">
    <label for="artist">Artist:</label>
    <input type="text" id="artist" name="artist">
    <label for="genre">Genre:</label>
    <input type="text" id="genre" name="genre">
    <label for="length">Length (in seconds):</label>
    <input type="number" id="length" name="length">
    <input type="submit" value="Add Song">
  </form>

  <button onclick="sortAndSearch(sortByTitle, 'title')">Sort by Title</button>
  <button onclick="sortAndSearch(sortByArtist, 'artist')">Sort by Artist</button>
  <button onclick="sortAndSearch(sortByGenre, 'genre')">Sort by Genre</button>

<div id="songs"></div>
  <script id="songTemplate" type="text/template">
    <div class="song-item">
      <span>{title} by {artist}, Genre: {genre}, Length: {length}s</span>
      <a href="{{ site.baseurl }}/CPlaylist" class="add-to-playlist">Add to your playlists</a>
    </div>
  </script>


  <script>
    let songs = JSON.parse(localStorage.getItem('songs')) || [];

    function displaySongs(songs) {
      const songsDiv = document.getElementById('songs');
      songsDiv.innerHTML = '';
      const template = document.getElementById('songTemplate').innerText;
      songs.forEach(song => {
        const songDiv = document.createElement('div');
        songDiv.innerHTML = template.replace('{title}', song.title).replace('{artist}', song.artist).replace('{genre}', song.genre).replace('{length}', song.length);
        songDiv.querySelector('.add-to-playlist').addEventListener('click', function() {
          addToPlaylist(song);
        });
        songsDiv.appendChild(songDiv);
      });
    }

    function addToPlaylist(song) {
      console.log('Adding song to playlist:', song);
    }

    function addSong(song) {
      songs.push(song);
      localStorage.setItem('songs', JSON.stringify(songs));
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

    function sortAndSearch(sortFunction, searchField) {
      const searchText = prompt("Enter search text:").toLowerCase();
      let sortedSongs = sortFunction();
      if (searchText !== null && searchText !== '') {
        sortedSongs = sortedSongs.filter(song => song[searchField].toLowerCase().includes(searchText));
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

    displaySongs(songs);
  </script>
</body>
</html>

<p> Fearful Cold War Preparations
Model: GPT-4
User
Rephrase: The main point of the article is to discuss the growing concern and preparations for survival under atomic attack during the Cold War era. It highlights the opinions and discussions of individuals regarding fallout shelters and the potential devastation of an atomic attack. The article also emphasizes the importance of civil defense and the government's efforts to promote and facilitate shelter-building initiatives.

Some of the recommendations mentioned in the article include:

The need for an adequate national system of fallout shelters to reduce casualties in the event of an atomic attack.
The importance of having a two-week supply of water and food in shelters, with specific suggestions on rationing and storage.
The necessity of an air-intake-exhaust system, a first-aid kit, flashlights, a battery radio, chemical toilets, and other essential items in shelters.
The promotion of affordable shelter options, such as simple backyard or basement shelters that can be built for $150 or less.
The involvement and assistance of state and local governments, private industry, and individuals in building shelters.
The need for industrial civil defense measures to protect private industry and vital records.
This article reflects the fear and preparations that were prevalent during the Cold War era when the threat of nuclear war between the United States and the Soviet Union loomed. The discussions, concerns, and efforts surrounding civil defense and the construction of shelters were a direct response to the perceived threat of an atomic attack. The article highlights the sense of urgency and the acknowledgment that survival and preparedness were crucial aspects of living during that time. —- make it casual 
ChatGPT

This piece is basically about the growing worries and all the "just-in-case" prepping during the Cold War, when folks thought a nuclear attack could happen any time. It shares people's thoughts and chats about nuclear fallout shelters and the horrific possibilities of an atomic attack. It also gives a big shout-out to civil defense and how the government was trying to help folks get their own shelters built.

Some cool suggestions the article throws out:

We need a solid network of fallout shelters nationwide so we can minimize the damage if an atomic attack happens.
Folks should have enough food and water stored up in their shelters for two weeks, along with some useful tips on how to save and split up supplies.
Air systems, first-aid kits, flashlights, battery-powered radios, chemical toilets and other must-haves should be in every shelter.
Cheap shelter options, like backyard or basement ones that cost 150 bucks or less, should be promoted.
State and local governments, private businesses, and everyday people should all get in on the action and help build shelters.
We need to make sure our industries are protected too, including their important records.
This article gives a glimpse into the fear and "be prepared" mindset that was so typical during the Cold War, when the US and the Soviet Union were in a nuclear staring contest. All the talk and plans around civil defense and getting shelters ready were reactions to the scary idea of an atomic attack. This piece really hammers home the feeling of urgency back then, and how important it was to be ready to survive. </p>