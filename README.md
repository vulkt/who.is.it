<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Guess the Name Game</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 50px;
    }

    h1 {
      margin-bottom: 20px;
    }

    label {
      font-weight: bold;
    }

    input {
      padding: 5px;
      margin-right: 10px;
    }

    button {
      padding: 8px 15px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 10px;
    }

    #message {
      margin-top: 20px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1> WHO'S THE MOST BEAUTIFUL GIRL ALIVE ???</h1>
  <label for="inputName">Enter a name to guess:</label>
  <input type="text" id="inputName" maxlength="20">
  <button onclick="checkGuess()">Submit</button>
  <p id="message"></p>

  <script>
    const targetName = 'jody' ||'Jody'||'JODY' ;
    let attempts = 0;

    function checkGuess() {
      const inputName = document.getElementById('inputName').value.trim().toLowerCase();

      if (inputName === targetName) {
        attempts++;
        document.getElementById('message').innerText = ` DAMN RIGHT Jody is indeed the most beautiful girl alive`;
        document.getElementById('inputName').disabled = true;
      } else if (inputName < targetName) {
        attempts++;
        document.getElementById('message').innerText = `Try again. IDIOT!!!`;
      } else {
        attempts++;
        document.getElementById('message').innerText = `Try again. IDIOT.!!!`;
      }
    }
  </script>
</body>
</html>
