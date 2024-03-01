<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Te iubesc, Mădy!</title>
<style>
  body, html {
    margin: 0;
    padding: 0;
    overflow: hidden;
    height: 100%;
    background: #000;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    font-family: Arial, sans-serif;
  }

  .heart {
    position: absolute;
    color: pink;
  }

  @keyframes fall {
    to {
      transform: translateY(100vh);
    }
  }

  .message {
    color: red;
    font-size: 2em;
    text-shadow: 2px 2px 4px #000;
    opacity: 0;
    animation: blink 4s infinite 2s;
    position: absolute;
    z-index: 1000;
  }

  @keyframes blink {
    50% {
      opacity: 1;
    }
  }
</style>
</head>
<body>
<div class="message">Te iubesc, Mădy!</div>

<script>
  function createHeart() {
    const heart = document.createElement('div');
    heart.classList.add('heart');
    heart.innerHTML = ['❤️', '💕', '💝'][Math.floor(Math.random() * 3)];
    heart.style.left = Math.random() * 100 + 'vw';
    heart.style.fontSize = Math.random() * 24 + 12 + 'px';
    heart.style.animation = `fall ${Math.random() * 5 + 2}s linear infinite`;
    document.body.appendChild(heart);

    setTimeout(() => {
      heart.remove();
    }, 5000);
  }

  setInterval(createHeart, 300);

</script>
</body>
</html>
