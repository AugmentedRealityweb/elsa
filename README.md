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
      opacity: 0;
      transition: opacity 1s ease-in-out;
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
      z-index: 1;
    }
  </style>
</head>
<body>
  <div class="image-container">
    <img src="https://i.pinimg.com/originals/bc/cd/8d/bccd8d514024b3547ef6d05843ce4864.gif" alt="First Image">
    <img src="https://i.giphy.com/shJoaSf7VpGnu.webp" alt="Second Image">
    <img src="https://i.giphy.com/WYoobOj0i6lJm.webp" alt="Third Image">
  </div>

  <div class="chat-widget">
    <elevenlabs-convai agent-id="5mz0QGMTS6vciobpmiXO"></elevenlabs-convai>
    <script src="https://elevenlabs.io/convai-widget/index.js" async></script>
  </div>
  <script>
    const images = document.querySelectorAll('.image-container img');
    let currentIndex = 0;

    function showNextImage() {
      images[currentIndex].style.opacity = "0";
      currentIndex = (currentIndex + 1) % images.length;
      images[currentIndex].style.opacity = "1";
    }

    setInterval(showNextImage, 4000);
  </script>
</body>
</html>
