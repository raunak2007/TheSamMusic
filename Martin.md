<!DOCTYPE html>
<html>
<head>
  <title>Playlist</title>
  <style>
    table {
      width: 100%;
      border-collapse: collapse;
    }

    th, td {
      padding: 8px;
      text-align: left;
      border-bottom: 1px solid #ddd;
    }

    th {
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Playlist</h1>
  <table id="playlist">
    <thead>
      <tr>
        <th onclick="sortTable(0)">Artist</th>
        <th onclick="sortTable(1)">Title</th>
        <th onclick="sortTable(2)">Date</th>
        <th onclick="sortTable(3)">Duration</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Iann Dior</td>
        <td>Songs</td>
        <td>2022-01-15</td>
        <td>3:20</td>
      </tr>
      <tr>
        <td>Post Malone</td>
        <td>Circles</td>
        <td>2019-08-30</td>
        <td>3:34</td>
      </tr>
      <tr>
        <td>Taylor Swift</td>
        <td>Love Story</td>
        <td>2008-09-12</td>
        <td>3:55</td>
      </tr>
      <tr>
        <td>Billie Eilish</td>
        <td>Bad Guy</td>
        <td>2019-03-29</td>
        <td>3:14</td>
      </tr>
      <tr>
        <td>Ed Sheeran</td>
        <td>Shape of You</td>
        <td>2017-01-06</td>
        <td>3:53</td>
      </tr>
      <tr>
        <td>Ariana Grande</td>
        <td>Thank U, Next</td>
        <td>2018-11-03</td>
        <td>3:27</td>
      </tr>
    </tbody>
  </table>

  <script>
    function sortTable(columnIndex) {
      var table, rows, switching, i, x, y, shouldSwitch;
      table = document.getElementById("playlist");
      switching = true;

      while (switching) {
        switching = false;
        rows = table.getElementsByTagName("tr");

        for (i = 1; i < (rows.length - 1); i++) {
          shouldSwitch = false;

          x = rows[i].getElementsByTagName("td")[columnIndex];
          y = rows[i + 1].getElementsByTagName("td")[columnIndex];

          if (x.innerHTML.toLowerCase() > y.innerHTML.toLowerCase()) {
            shouldSwitch = true;
            break;
          }
        }

        if (shouldSwitch) {
          rows[i].parentNode.insertBefore(rows[i + 1], rows[i]);
          switching = true;
        }
      }
    }
  </script>
</body>
</html>
