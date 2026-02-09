<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Be My Valentine</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #ffe6e6;
      margin: 0;
      padding: 0;
    } 

    .container {
      margin-top: 50px;
    }

    #question {
      font-size: 24px;
      margin-bottom: 10px;
    }

    #nameForm, #valentineMessage {
      display: none;
    }

    input[type="text"] {
      padding: 10px;
      font-size: 18px;
      border: 1px solid #c4c4c4;
      border-radius: 8px;
      outline: none;
      text-align: center;
    }

    button {
      padding: 10px 25px;
      font-size: 20px;
      background-color: #ff94c2;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    button:hover {
      background-color: #ff4dab;
    }

    #valentineMessage {
      font-size: 32px;
      color: #ff4078;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Hi there! 💖</h1>
    <p id="question">What's your name?</p>
    <div id="nameForm">
      <input type="text" id="nameInput" placeholder="Type your name here...">
      <br><br>
      <button onclick="checkName()">Submit</button>
    </div>
    <div id="valentineMessage">
        <p>Will you be my Valentine? 🌹</p>
        <button onclick="alert('Yay! You said yes! ❤️')">Yes</button>
    </div>
  </div>

  <script>
    document.getElementById("nameForm").style.display = "block";

    function checkName() {
      const nameInput = document.getElementById("nameInput").value.trim();
      if (nameInput.toLowerCase() === "your baby") {
        document.getElementById("nameForm").style.display = "none";
        document.getElementById("valentineMessage").style.display = "block";
      } else {
        alert("Oops! You need to type 'your baby' to continue! 💕");
      }
    }
  </script>
</body>
</html>