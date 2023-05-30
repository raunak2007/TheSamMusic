<div data-aos="fade-right">
<h2>Musical Preference Quiz</h2>
<div id="question1">
<p>Do you prefer modern music?</p>
<button onclick="answer(true)">Yes</button>
<button onclick="answer(false)">No</button>
</div>
<div id="question2" style="display: none">
<p>Do you enjoy music with a fast tempo?</p>
<button onclick="answer(true)">Yes</button>
<button onclick="answer(false)">No</button>
</div>
<div id="question3" style="display: none">
<p>Do you like music with lyrics?</p>
<button onclick="answer(true)">Yes</button>
<button onclick="answer(false)">No</button>
</div>
<div id="question4" style="display: none">
<p>Do you prefer instrumental music?</p>
<button onclick="answer(true)">Yes</button>
<button onclick="answer(false)">No</button>
</div>
<div id="question5" style="display: none">
<p>Do you enjoy electronic music?</p>
<button onclick="answer(true)">Yes</button>
<button onclick="answer(false)">No</button>
</div>
<div id="question6" style="display: none">
<p>Do you prefer music from different cultures?</p>
<button onclick="answer(true)">Yes</button>
<button onclick="answer(false)">No</button>
</div>
<div id="result" style="display: none"></div>
</div>


<div style="padding: 10px;"></div>


<div data-aos="fade-right">
<h3>Which music preference would you like to talk about?</h3>
<select id="music-select">
  <option>90's Hip-Hop</option>
  <option>Rock N Roll</option>
  <option>Modern Rap/Street Drill</option>
  <option>UK Drill</option>
  <option>Classical Music</option>
  <option>Classical Jazz</option>
  <option>Pop Music</option>
  <option>Old Style Soul</option>
  <option>EDM</option>
  <option>Country/Folk</option>
  <option>Blues</option>
  <option>K-POP</option>
  <option>Funk</option>
  <option>Salsa</option>
  <option>Goth</option>
  <option>Latin/Spanish</option>
  <option>French Classical</option>
  <option>Jamaican</option>
  <option>Japanese Classical</option>
  <option>Bollywood Music</option>
  <option>Iranian Music</option>
  <option>Chinese Folk</option>
  <option>Opera</option>
  <option>Heavy Metal</option>
  <option>2000's Rap</option>
  <option>Mashed Soul & Rap</option>
  <option>Upbeat</option>
  <option>Poprock</option>
  <option>Hawaiian/Islander Music</option>
</select>
<button id="save-button">Save</button>
<p>Your current music preference is <span id="saved-music"></span><br>Reload to show most recent music taste you want to pursue!</p>
</div>


<script>
// JavaScript code that listens to a click on the "Save" button and saves the selected value to local storage
const saveButton = document.getElementById('save-button');
const musicSelect = document.getElementById('music-select');
//empty list
let currentMusic = [];
function displaySavedMusic(selectedMusic) {
  //spacing
  let x = " " + selectedMusic;
  //pushes the selectedMusic into the empty list
  currentMusic.push(x);
  //identifying span element in lines 80-81
  let spaan = document.getElementById("saved-music");
  //setting the text to the music genre selected, innerHTML changes what is between the span text.
  spaan.innerHTML = currentMusic;
};
saveButton.addEventListener('click', function() {
  const selectedMusic = musicSelect.value;
  localStorage.setItem('selectedMusic', selectedMusic);
  displaySavedMusic(selectedMusic);
}
)
// JavaScript code that retrieves and displays the saved value when the page is loaded
const savedMusic = localStorage.getItem('selectedMusic');
if (savedMusic) {
  displaySavedMusic(savedMusic);
}
</script>


<script>
    // Music list
var musicList = ["90's Hip-Hop", "Rock N Roll", "Modern Rap/Street Drill", /* Add the rest of the genres */];
// Sets the current question
var currentQuestion = 1;
// Array for the answers to the questions
var answers = [];


// Function for the questions
function answer(response) {
  // Finds the current answer and hides or unhides it
  answers[currentQuestion - 1] = response;
  document.getElementById("question" + currentQuestion).style.display = "none";
  currentQuestion++;


  if (currentQuestion <= 6) {
    document.getElementById("question" + currentQuestion).style.display = "block";
  } else {
    removeMusicGenres(answers[0], answers[1], answers[2], answers[3], answers[4], answers[5]);
    document.getElementById("result").style.display = "block";
    document.getElementById("result").innerHTML = "Based on your answers, we recommend the following music genres: " + musicList.join(", ");
  }
}


function removeMusicGenres(genre1, genre2, genre3, genre4, genre5, genre6) {
  musicList = musicList.filter(item => item !== genre1 && item !== genre2 && item !== genre3 && item !== genre4 && item !== genre5 && item !== genre6);
}


function removeMusicGenres(likesFast, likesSlow, likesInstrumental, likesElectronic, likesVocals, likesLyrical) {
  if (likesFast) {
    musicList = musicList.filter(genre => genre !== "Classical Music" && genre !== "Classical Jazz" && genre !== "Old Style Soul" && genre !== "Blues" && genre !== "French Classical" && genre !== "Opera" && genre !== "Hawaiian/Islander Music");
  }


  if (likesSlow) {
    musicList = musicList.filter(genre => genre !== "EDM" && genre !== "K-POP" && genre !== "Funk" && genre !== "Salsa" && genre !== "Heavy Metal" && genre !== "Upbeat");
  }


  if (likesInstrumental) {
    musicList = musicList.filter(genre => genre !== "Modern Rap/Street Drill" && genre !== "K-POP" && genre !== "2000's Rap" && genre !== "Mashed Soul & Rap" && genre !== "Poprock");
  }


  if (likesElectronic) {
    musicList = musicList.filter(genre => genre !== "Classical Music" && genre !== "Classical Jazz" && genre !== "Old Style Soul" && genre !== "Blues" && genre !== "Country/Folk" && genre !== "French Classical" && genre !== "Japanese Classical" && genre !== "Opera" && genre !== "Hawaiian/Islander Music");
  }


  if (likesVocals) {
    musicList = musicList.filter(genre => genre !== "EDM" && genre !== "Classical Music" && genre !== "Classical Jazz" && genre !== "Country/Folk" && genre !== "Chinese Folk");
  }


  if (likesLyrical) {
    musicList = musicList.filter(genre => genre !== "EDM" && genre !== "K-POP" && genre !== "Funk" && genre !== "Salsa" && genre !== "Heavy Metal" && genre !== "Upbeat" && genre !== "Poprock" && genre !== "Hawaiian/Islander Music");
  }
}
// The result of the function
document.getElementById("result").innerHTML = "Based on your answers, we recommend the following music genres: " + musicList.join(", ");


</script>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {font-family: Arial, Helvetica, sans-serif;}
* {box-sizing: border-box;}
/* Button used to open the chat form - fixed at the bottom of the page */
.open-button {
  background-color: #555;
  color: white;
  padding: 16px 20px;
  border: none;
  cursor: pointer;
  opacity: 0.8;
  position: fixed;
  bottom: 23px;
  right: 28px;
  width: 280px;
}
/* The popup chat - hidden by default */
.chat-popup {
  display: none;
  position: fixed;
  bottom: 0;
  right: 15px;
  border: 3px solid #f1f1f1;
  z-index: 9;
}
/* Add styles to the form container */
.form-container {
  max-width: 300px;
  padding: 10px;
  background-color: white;
}
/* Full-width textarea */
.form-container textarea {
  width: 100%;
  padding: 15px;
  margin: 5px 0 22px 0;
  border: none;
  background: white;
  resize: none;
  min-height: 200px;
}
/* When the textarea gets focus, do something */
.form-container textarea:focus {
  background-color: #ddd;
  outline: none;
}
/* Set a style for the submit/send button */
.form-container .btn {
  background-color: #04AA6D;
  color: white;
  padding: 16px 20px;
  border: none;
  cursor: pointer;
  width: 100%;
  margin-bottom:10px;
  opacity: 0.8;
}
/* Add a red background color to the cancel button */
.form-container .cancel {
  background-color: red;
}
/* Add some hover effects to buttons */
.form-container .btn:hover, .open-button:hover {
  opacity: 1;
}
/* Add the new rule here */
.form-container h1 {
  color: black;
}
/* Add the new rule here */
.form-container label {
  color: black;
}
</style>
</head>
<body>

<h2>Talk Music with SAM</h2>
<p>Click on the button at the bottom of this page to open the chat form.</p>
<p>Your message will be stored below! Talk Music CONVO!!!! Enjoy!</p>
<hr>
<button class="open-button" onclick="openForm()">Chat with SAM</button>

<div class="chat-popup" id="myForm">
  <form class="form-container" onsubmit="event.preventDefault(); sendMessage();">
    <h1>Chat with SAM</h1>
    <label for="msg"><b>Message</b></label>
    <textarea id="message-input" placeholder="Type message.." name="msg" required></textarea>
    <button type="submit" class="btn">Send with SAM</button>
    <button type="button" class="btn cancel" onclick="closeForm()">Close SAM</button>
  </form>
</div>

<div id="message-container">
</div>

<script>
function openForm() {
  document.getElementById("myForm").style.display = "block";
}

function closeForm() {
  document.getElementById("myForm").style.display = "none";
}

function sendMessage() {
  const messageInput = document.getElementById("message-input");
  const message = 'CSP Period 5 User Says: ' + messageInput.value;
  
  const messages = JSON.parse(localStorage.getItem('messages') || '[]');
  messages.push(message);
  localStorage.setItem('messages', JSON.stringify(messages));

  displayMessage(message);
  messageInput.value = '';
}

function displayMessage(message) {
  const messageContainer = document.getElementById("message-container");
  const messageElement = document.createElement("p");
  messageElement.textContent = message;
  messageContainer.appendChild(messageElement);
}
// Fetch messages from localStorage and display them
const storedMessages = JSON.parse(localStorage.getItem('messages') || '[]');
storedMessages.forEach(displayMessage);

// Add the event listener to the message input field
document.getElementById("message-input").addEventListener("keydown", function(event) {
  if (event.key === "Enter") {
    event.preventDefault();
    sendMessage();
  }
});
</script>

</body>
</html>

JHON CENA
