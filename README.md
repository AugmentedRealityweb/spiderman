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
      overflow: hidden;
    }

    .image-container img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      position: absolute;
      animation: fade 8s infinite;
    }

    .image-container img:nth-child(2) {
      animation-delay: 4s;
    }

    @keyframes fade {
      0% { opacity: 1; }
      45% { opacity: 1; }
      55% { opacity: 0; }
      100% { opacity: 0; }
    }

    .chat-widget {
      position: fixed;
      top: 40%;
      left: 30%;
      transform: translate(-50%, -50%);
      width: 450px;
      height: 500px;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      background-color: transparent;
      z-index: 2;
    }
  </style>
</head>
<body>
  <div class="image-container">
    <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExd2VtcHdiZHpjMmgybTl5eWtvMjdnMnVzbmU3eG80OW5kemJsOGc0NiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/wuU9Hvp5wF7xe/giphy.webp" alt="First GIF">
    <img src="https://i.pinimg.com/originals/32/64/5e/32645e1a0642ce7fc4d952dde6e598a8.gif" alt="Second GIF">
  </div>
  <div class="chat-widget">
    <elevenlabs-convai agent-id="sNEfrsQUklzPW2Hu6VGg"></elevenlabs-convai>
    <script src="https://elevenlabs.io/convai-widget/index.js" async></script>
  </div>
</body>
</html>
