<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    body {
      margin: 0;
      padding: 0;
      background: #000;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      position: relative;
    }

    .image-container {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }

    .image-container img {
      max-width: 100%;
      max-height: 100%;
      object-fit: cover;
      border: 2px solid #fff;
    }

    .chat-widget {
      position: absolute;
      bottom: 10%;
      width: 80%;
      max-width: 400px;
    }
  </style>
</head>
<body>
  <div class="image-container">
    <img src="https://i.pinimg.com/originals/bc/cd/8d/bccd8d514024b3547ef6d05843ce4864.gif" alt="First Image">
  </div>

  <div class="chat-widget">
    <elevenlabs-convai agent-id="5mz0QGMTS6vciobpmiXO"></elevenlabs-convai>
    <script src="https://elevenlabs.io/convai-widget/index.js" async></script>
  </div>
</body>
</html>
