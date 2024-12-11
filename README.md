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
      display: flex;
      justify-content: center;
      align-items: center;
      height: 50%;
    }

    .image-container img {
      max-width: 2000px;
      max-height: 2080px;
      object-fit: cover;
      border: 2px solid #fff;
    }

    .chat-widget {
      width: 80%;
      max-width: 400px;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 20%;
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
