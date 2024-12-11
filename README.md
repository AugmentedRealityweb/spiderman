<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    body {
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #000;
      flex-direction: column;
    }

    .image-container {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
    }

    .image-container img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .chat-widget {
      width: 80%;
      max-width: 400px;
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 1;
    }
  </style>
</head>
<body>
  <div class="image-container">
    <img src="https://i.giphy.com/1qErVv5GVUac8uqBJU.webp" alt="Background Image">
  </div>
  <div class="chat-widget">
    <elevenlabs-convai agent-id="sNEfrsQUklzPW2Hu6VGg"></elevenlabs-convai>
    <script src="https://elevenlabs.io/convai-widget/index.js" async></script>
  </div>
</body>
</html>
