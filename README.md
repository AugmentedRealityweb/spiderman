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
    top: 40%;
    left: 30%;
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
    <img src="https://64.media.tumblr.com/a0187c8083520ea4434a76bbec8154d7/tumblr_pxyuq0F23d1ql43puo1_400.gifv">
  </div>
  <div class="chat-widget">
    <elevenlabs-convai agent-id="sNEfrsQUklzPW2Hu6VGg"></elevenlabs-convai>
    <script src="https://elevenlabs.io/convai-widget/index.js" async></script>
  </div>
</body>
</html>
