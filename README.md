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
      z-index: 1;
    }

    .image-container img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .chat-widget {
    position: fixed;
    top: 20%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 450px;
    height: 50px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    background-color: transparent;
    z-index: 1;
}
  </style>
</head>
<body>
  <div class="image-container">
    <img src="https://i.pinimg.com/originals/32/64/5e/32645e1a0642ce7fc4d952dde6e598a8.gif">
  </div>
  <div class="chat-widget">
    <elevenlabs-convai agent-id="sNEfrsQUklzPW2Hu6VGg"></elevenlabs-convai>
    <script src="https://elevenlabs.io/convai-widget/index.js" async></script>
  </div>
</body>
</html>
