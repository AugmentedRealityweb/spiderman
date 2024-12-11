<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    body {
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #000;
    }

    .image-container {
      margin-bottom: 20px;
    }

    .image-container img {
      max-width: 90%;
      max-height: 80%;
      border: 2px solid #fff;
    }

    .chat-widget {
      width: 80%;
      max-width: 400px;
      margin-top: auto;
      margin-bottom:40px;
    }
  </style>
</head>
<body>
  <div class="image-container">
    <img src="https://i.giphy.com/1qErVv5GVUac8uqBJU.webp" alt="Second Image">
  </div>
  <div class="chat-widget">
    <elevenlabs-convai agent-id="sNEfrsQUklzPW2Hu6VGg"></elevenlabs-convai>
    <script src="https://elevenlabs.io/convai-widget/index.js" async></script>
  </div>
</body>
</html>
