# Sumit_
I developed the googleChrome Extension using a technologies with html, CSS, and JavaScript 

# html 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DadJokes</title>
</head>
<body>
  <p id="jokeElement">Loading.. </p>
  <script src="popup.js"></script>
</body>
</html>

# js
fetch('https://icanhazdadjoke.com/slack')
.then(data => data.json())
.then(jokeData => {
  const jokeText = jokeData.attachments[0].text;
  const jokeElement = document.getElementById('jokeElement');

  jokeElement.innerHTML = jokeText;
})

# manifest.json
{
  "name":"DadJokes",
  "version":"0.0.1",
  "manifest_version": 2,
  "browser_action": {
    "default_popup":"popup.html",
    "default_icon":"logo2.png"
  },
  "icons":{
    "128": "logo2.png"
  },
  "permissions":["activeTab"]
}

# logo 

add a logo with .png
