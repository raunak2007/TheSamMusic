<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Add Song</title>

  <style>
    /* Form container */
    #song-form {
      max-width: 400px;
      margin: 0 auto;
      padding: 20px;
      background-color: #f4f4f4;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    /* Form fields */
    #song-form div {
      margin-bottom: 15px;
    }

    #song-form label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
      color: #000;
    }

    #song-form input[type="text"] {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 3px;
      box-sizing: border-box;
    }

    /* Submit button */
    #song-form input[type="submit"] {
      background-color: #4CAF50;
      color: #fff;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
      border-radius: 3px;
    }

    #song-form input[type="submit"]:hover {
      background-color: #45a049;
    }
  </style>
</head>

<body>
  <form id="song-form">
    <div>
      <label for="playlist">Playlist:</label>
      <input type="text" id="playlist" name="playlist" required>
    </div>
    <div>
      <label for="artist">Artist:</label>
      <input type="text" id="artist" name="artist" required>
    </div>
    <div>
      <label for="title">Title:</label>
      <input type="text" id="title" name="title" required>
    </div>
    <div>
      <label for="duration">Duration:</label>
      <input type="text" id="duration" name="duration" required>
    </div>
    <div>
      <input type="submit" value="Add Song">
    </div>
  </form>
</body>

</html>
