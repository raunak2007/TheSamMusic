As the project manager for our music storing software project, my role is crucial in ensuring the successful development and delivery of the product. Here are some key responsibilities and tasks that I will undertake:

**Project Planning:** I will be responsible for defining project goals, scope, and objectives. This involves understanding the requirements of the music storing software, identifying key features, and determining the project timeline and resources needed.

**Team Coordination:** I will assemble and lead a team of developers, designers, and testers. My role is to ensure effective communication and collaboration within the team, assign tasks and responsibilities, and monitor progress to ensure timely completion of milestones.

**Requirement Analysis:** Working closely with stakeholders, including users and management, you will gather requirements for the music storing software. This involves understanding user needs, defining features such as search functionality, playlist management, and user interface requirements.

**Risk Management:** Identifying potential risks and challenges that could impact project success is essential. I will proactively assess risks, develop mitigation strategies, and monitor their implementation to minimize project setbacks.

**Resource Management:** As the project progresses, you will manage project resources, including budget, equipment, and software licenses. Ensuring that the team has the necessary tools and resources to complete their tasks efficiently is crucial to project success.

**Progress Monitoring:** Tracking project progress against the defined timeline and milestones is one of my responsibilities. Regularly communicating with the team, addressing any roadblocks, and ensuring that project deliverables are on track are essential aspects of progress monitoring.

**Quality Assurance:** I will oversee the quality assurance process to ensure that the music storing software meets the defined standards and user requirements. This includes conducting testing, reviewing design and code, and facilitating user feedback to improve the software's functionality and user experience.

**Stakeholder Management:** As the project manager, I will engage with stakeholders, such as users and management, to provide project updates, gather feedback, and address any concerns. Managing expectations and maintaining positive relationships with stakeholders are important for project success.

**Project Documentation:** I will ensure proper documentation of project requirements, specifications, design decisions, and other relevant information. This documentation serves as a valuable reference and knowledge base for the team and stakeholders.

**Project Delivery:** Ultimately, my role is to oversee the successful delivery of the music storing software. This involves coordinating the final testing, deployment, and launch activities, ensuring a smooth transition from development to the production environment.


# What I Have Done So Far...
- So far I have created the log-in page, and plan on fixing the "sign-up" page as well. 
- I am also working on the search feature, and the template code for that may be seen below.

<!DOCTYPE html>
<html>
<head>
  <title>Playlist Manager</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }

    h1 {
      text-align: center;
    }

    .search-container {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 20px;
    }

    .search-input {
      padding: 10px;
      width: 300px;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 16px;
    }

    .search-button {
      padding: 10px 20px;
      margin-left: 10px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
    }

    #playlist {
      list-style-type: none;
      padding: 0;
    }

    .song-item {
      display: flex;
      align-items: center;
      margin-bottom: 10px;
      cursor: move;
      padding: 10px;
      background-color: #f2f2f2;
      border-radius: 4px;
    }

    .song-item:hover {
      background-color: #e0e0e0;
    }

    .song-item img {
      width: 40px;
      height: 40px;
      margin-right: 10px;
      border-radius: 50%;
    }

    .song-title {
      font-weight: bold;
      color: black;
    }
  </style>
</head>
<body>
  <h1>Playlist Manager</h1>

  <div class="search-container">
    <input type="text" id="search-input" class="search-input" placeholder="Search for a song...">
    <button id="search-button" class="search-button">Search</button>
  </div>

  <ul id="playlist">
    <!-- Song items will be dynamically added here -->
  </ul>

  <script>
    const searchInput = document.getElementById('search-input');
    const searchButton = document.getElementById('search-button');
    const playlist = document.getElementById('playlist');

    searchButton.addEventListener('click', () => {
      const searchTerm = searchInput.value;
      searchSongs(searchTerm);
    });

    function searchSongs(searchTerm) {
      // You can make a request to your backend API or directly to the Spotify API for song search
      // Replace the code below with your actual API request
      const songs = [
        { title: "Circles - Post Malone", image: "https://source.unsplash.com/random/40x40" },
        { title: "God's Plan - Drake", image: "https://source.unsplash.com/random/40x40" },
        { title: "XO TOUR Llif3 - Lil Uzi Vert", image: "https://source.unsplash.com/random/40x40" },
        { title: "Blinding Lights - The Weeknd", image: "https://source.unsplash.com/random/40x40" }
      ];

      displaySearchResults(songs);
    }

    function displaySearchResults(songs) {
      playlist.innerHTML = '';

      songs.forEach(song => {
        const songItem = document.createElement('li');
        songItem.className = 'song-item';

        const songImage = document.createElement('img');
        songImage.src = song.image;
        songItem.appendChild(songImage);

        const songTitle = document.createElement('span');
        songTitle.className = 'song-title';
        songTitle.textContent = song.title;
        songItem.appendChild(songTitle);

        playlist.appendChild(songItem);
      });
    }

    let draggedItem = null;

    function dragStart(event) {
      draggedItem = event.target;
      event.dataTransfer.effectAllowed = 'move';
    }

    function dragOver(event) {
      event.preventDefault();
      event.dataTransfer.dropEffect = 'move';
    }

    function drop(event) {
      event.preventDefault();

      // Move the dragged item to the drop target
      const dropTarget = event.target;
      if (dropTarget.classList.contains('song-item')) {
        const parent = dropTarget.parentNode;
        const temp = document.createElement('div');
        parent.insertBefore(temp, dropTarget);
        parent.insertBefore(draggedItem, temp);
        parent.removeChild(temp);
      }
    }
  </script>
</body>
</html>




<html>
<head>
  <title>Music Playlist</title>
  <style>
    table {
      border-collapse: collapse;
      width: 100%;
    }
    
    th, td {
      text-align: left;
      padding: 8px;
    }
    
    th {
      cursor: pointer;
    }
    
    .sortable-header::after {
      content: '\25B2';
      float: right;
      margin-left: 5px;
    }
    
    .sortable-header.asc::after {
      content: '\25BC';
    }
  </style>
</head>
<body>
  <table id="musicTable">
    <thead>
      <tr>
        <th onclick="sortTable('title')">Title</th>
        <th onclick="sortTable('artist')">Artist</th>
        <th onclick="sortTable('duration')">Duration (seconds)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Rockstar</td>
        <td>Post Malone</td>
        <td>218</td>
      </tr>
      <tr>
        <td>God's Plan</td>
        <td>Drake</td>
        <td>198</td>
      </tr>
      <tr>
        <td>Stronger</td>
        <td>Kanye West</td>
        <td>311</td>
      </tr>
      <tr>
        <td>Mask Off</td>
        <td>Future</td>
        <td>227</td>
      </tr>
      <tr>
        <td>Circles</td>
        <td>Post Malone</td>
        <td>215</td>
      </tr>
      <tr>
        <td>One Dance</td>
        <td>Drake</td>
        <td>173</td>
      </tr>
      <tr>
        <td>Heartless</td>
        <td>Kanye West</td>
        <td>228</td>
      </tr>
      <tr>
        <td>Low Life</td>
        <td>Future</td>
        <td>315</td>
      </tr>
    </tbody>
  </table>
  
  <script>
    // Function to sort the table based on the selected column
    function sortTable(columnName) {
      const table = document.getElementById('musicTable');
      const rows = Array.from(table.tBodies[0].getElementsByTagName('tr'));
      const headerRow = table.getElementsByTagName('thead')[0].getElementsByTagName('tr')[0];
      const isAscending = !headerRow.classList.contains('asc');
      
      rows.sort((rowA, rowB) => {
        const cellA = rowA.querySelector(`td:nth-child(${getColumnIndex(columnName)})`).innerText;
        const cellB = rowB.querySelector(`td:nth-child(${getColumnIndex(columnName)})`).innerText;
        
        return isAscending ? cellA.localeCompare(cellB) : cellB.localeCompare(cellA);
      });
      
      rows.forEach(row => table.tBodies[0].appendChild(row));
      headerRow.classList.toggle('asc');
    }
  
    // Helper function to get the index of the selected column
    function getColumnIndex(columnName) {
      const table = document.getElementById('musicTable');
      const headerRow = table.getElementsByTagName('thead')[0].getElementsByTagName('tr')[0];
      const headers = Array.from(headerRow.getElementsByTagName('th'));
      
      return headers.findIndex(header => header.innerText.toLowerCase() === columnName.toLowerCase()) + 1;
    }
  </script>
</body>
</html>


<html>
<head>
  <title>Playlist Manager</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }

    h1 {
      text-align: center;
    }

    #playlist {
      list-style-type: none;
      padding: 0;
    }

    .song-item {
      display: flex;
      align-items: center;
      margin-bottom: 10px;
      cursor: move;
      padding: 10px;
      background-color: #f2f2f2;
      border-radius: 4px;
    }

    .song-item:hover {
      background-color: #e0e0e0;
    }

    .song-item img {
      width: 40px;
      height: 40px;
      margin-right: 10px;
      border-radius: 50%;
    }

    .song-title {
      font-weight: bold;
      color: black; /* Set font color to black */
    }
  </style>
</head>
<body>
  <h1>Playlist Manager</h1>

  <ul id="playlist">
    <li class="song-item" draggable="true" ondragstart="dragStart(event)" ondragover="dragOver(event)" ondrop="drop(event)">
      <img src="https://source.unsplash.com/random/40x40" alt="Song 1">
      <span class="song-title">Circles - Post Malone</span>
    </li>
    <li class="song-item" draggable="true" ondragstart="dragStart(event)" ondragover="dragOver(event)" ondrop="drop(event)">
      <img src="https://source.unsplash.com/random/40x40" alt="Song 2">
      <span class="song-title">God's Plan - Drake</span>
    </li>
    <li class="song-item" draggable="true" ondragstart="dragStart(event)" ondragover="dragOver(event)" ondrop="drop(event)">
      <img src="https://source.unsplash.com/random/40x40" alt="Song 3">
      <span class="song-title">XO TOUR Llif3 - Lil Uzi Vert</span>
    </li>
    <li class="song-item" draggable="true" ondragstart="dragStart(event)" ondragover="dragOver(event)" ondrop="drop(event)">
      <img src="https://source.unsplash.com/random/40x40" alt="Song 4">
      <span class="song-title">Blinding Lights - The Weeknd</span>
    </li>
  </ul>

  <script>
    let draggedItem = null;

    function dragStart(event) {
      draggedItem = event.target;
      event.dataTransfer.effectAllowed = 'move';
    }

    function dragOver(event) {
      event.preventDefault();
      event.dataTransfer.dropEffect = 'move';
    }

    function drop(event) {
      event.preventDefault();

      // Move the dragged item to the drop target
      const dropTarget = event.target;
      if (dropTarget.classList.contains('song-item')) {
        const parent = dropTarget.parentNode;
        const temp = document.createElement('div');
        parent.insertBefore(temp, dropTarget);
        parent.insertBefore(draggedItem, temp);
        parent.removeChild(temp);
      }
    }
  </script>
</body>
</html>


