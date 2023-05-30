<html>
<head>
    <title>Song Search</title>
    <style>
        table {
            border-collapse: collapse;
            width: 100%;
        }
        th, td {
            text-align: left;
            padding: 8px;
        }
        tr:nth-child(even) {
            background-color: teal;
            color: gold;
        }
        #searchInput {
            width: 100%;
            padding: 12px 20px;
            margin-bottom: 12px;
        }
    </style>
</head>
<body>
    <h1>Song Search</h1>

    <input type="text" id="searchInput" placeholder="Search for a song or artist...">
    
   <table id="songTable">
    <tr>
        <th>Song</th>
        <th>Artist</th>
        <th>Duration</th>
        <th>Date</th>
    </tr>
    <tr>
        <td>Love Story</td>
        <td>Taylor Swift</td>
        <td>3:56</td>
        <td>2008</td>
    </tr>
    <tr>
        <td>Circles</td>
        <td>Post Malone</td>
        <td>3:34</td>
        <td>2019</td>
    </tr>
    <tr>
        <td>Roar</td>
        <td>Katy Perry</td>
        <td>3:42</td>
        <td>2013</td>
    </tr>
    <tr>
        <td>Sorry</td>
        <td>Justin Bieber</td>
        <td>3:20</td>
        <td>2015</td>
    </tr>
    <tr>
        <td>Drip Too Hard</td>
        <td>Lil Baby</td>
        <td>2:25</td>
        <td>2018</td>
    </tr>
    <tr>
        <td>Blank Space</td>
        <td>Taylor Swift</td>
        <td>3:51</td>
        <td>2014</td>
    </tr>
    <tr>
        <td>Rockstar</td>
        <td>Post Malone</td>
        <td>3:38</td>
        <td>2017</td>
    </tr>
    <tr>
        <td>Firework</td>
        <td>Katy Perry</td>
        <td>3:48</td>
        <td>2010</td>
    </tr>
    <tr>
        <td>Yummy</td>
        <td>Justin Bieber</td>
        <td>3:30</td>
        <td>2020</td>
    </tr>
    <tr>
        <td>Woah</td>
        <td>Lil Baby</td>
        <td>3:03</td>
        <td>2020</td>
    </tr>
    <tr>
        <td>Shake It Off</td>
        <td>Taylor Swift</td>
        <td>3:39</td>
        <td>2014</td>
    </tr>
    <tr>
        <td>Bad Blood</td>
        <td>Taylor Swift</td>
        <td>3:19</td>
        <td>2014</td>
    </tr>
</table>
    <script>
        const searchInput = document.getElementById('searchInput');
        const table = document.getElementById('songTable');
        const rows = table.getElementsByTagName('tr');
        
        searchInput.addEventListener('keyup', function() {
            const searchTerm = searchInput.value.toLowerCase();
            
            for (let i = 1; i < rows.length; i++) {
                const song = rows[i].getElementsByTagName('td')[0].textContent.toLowerCase();
                const artist = rows[i].getElementsByTagName('td')[1].textContent.toLowerCase();
                
                if (song.includes(searchTerm) || artist.includes(searchTerm)) {
                    rows[i].style.display = '';
                } else {
                    rows[i].style.display = 'none';
                }
            }
        });
    </script>
</body>
</html>
