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
    left: 20%;
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
    <img src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/6bddfaca-e177-478a-b606-4b55711caf9d/d7acy16-7f023f21-92ee-4b8b-8119-c81016caee1b.gif?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzZiZGRmYWNhLWUxNzctNDc4YS1iNjA2LTRiNTU3MTFjYWY5ZFwvZDdhY3kxNi03ZjAyM2YyMS05MmVlLTRiOGItODExOS1jODEwMTZjYWVlMWIuZ2lmIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.p95kmGJdxoVFXN40epNr1ntexC1-pebAkMPl1afCEzY">
  </div>
  <div class="chat-widget">
    <elevenlabs-convai agent-id="sNEfrsQUklzPW2Hu6VGg"></elevenlabs-convai>
    <script src="https://elevenlabs.io/convai-widget/index.js" async></script>
  </div>
</body>
</html>
