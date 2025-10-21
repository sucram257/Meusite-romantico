# Meusite-romantico<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Surpresa Romântica</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: #f8f8f8;
      font-family: Arial, sans-serif;
      overflow: hidden;
    }
    .container {
      text-align: center;
      padding: 20px;
    }
    .photo {
      width: 80%;
      max-width: 600px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
    .text {
      font-size: 1.2rem;
      color: #333;
      margin-top: 20px;
      line-height: 1.6;
    }
    .emoji {
      position: absolute;
      font-size: 2rem;
      animation: fall 5s infinite;
      pointer-events: none;
    }
    @keyframes fall {
      0% {
        top: -50px;
        opacity: 1;
      }
      100% {
        top: 100%;
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <img src="sua-foto.jpg" alt="Foto do Casal" class="photo">
    <div class="text">
      <p>Meu amor, cada momento ao seu lado é um sonho realizado.</p>
      <p>Te amo mais a cada dia. 💖</p>
    </div>
  </div>
  <audio autoplay loop>
    <source src="https://www.youtube.com/watch?v=hWadAXfH6Uc" type="audio/mp3">
    Seu navegador não suporta o elemento de áudio.
  </audio>
  <script>
    const emojis = ['💖', '😍', '😘', '💌', '💘', '💝'];
    setInterval(() => {
      const emoji = emojis[Math.floor(Math.random() * emojis.length)];
      const span = document.createElement('span');
      span.textContent = emoji;
      span.classList.add('emoji');
      span.style.left = `${Math.random() * 100}vw`;
      document.body.appendChild(span);
      setTimeout(() => {
        span.remove();
      }, 5000);
    }, 200);
  </script>
</body>
</html>
