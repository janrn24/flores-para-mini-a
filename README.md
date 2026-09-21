<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>21 de Septiembre 💛</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      background: linear-gradient(135deg, #fff9e6 0%, #ffecb3 100%);
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      overflow-x: hidden;
      padding: 20px;
    }

    .container {
      max-width: 600px;
      width: 100%;
    }

    h1 {
      color: #d4a373;
      font-size: 2rem;
      margin-bottom: 20px;
      text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
    }

    button {
      background-color: #ffb703;
      color: #fff;
      border: none;
      padding: 15px 32px;
      font-size: 1.2rem;
      font-weight: bold;
      border-radius: 50px;
      cursor: pointer;
      box-shadow: 0 4px 15px rgba(255, 183, 3, 0.4);
      transition: all 0.3s ease;
    }

    button:hover {
      background-color: #fb8500;
      transform: translateY(-3px) scale(1.05);
      box-shadow: 0 6px 20px rgba(251, 133, 0, 0.5);
    }

    button:active {
      transform: translateY(1px);
    }

    /* Mensaje final */
    .message {
      opacity: 0;
      transform: scale(0.5);
      transition: all 1s ease-in-out;
      margin-top: 25px;
      font-size: 2.2rem;
      color: #e07a5f;
      font-weight: bold;
      text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
    }

    .message.show {
      opacity: 1;
      transform: scale(1);
    }

    /* Contenedor del Ramo de Flores */
    .bouquet-container {
      position: relative;
      width: 280px;
      height: 320px;
      margin: 30px auto 10px;
      display: flex;
      justify-content: center;
      align-items: flex-end;
    }

    /* Tallo/Lazo del Ramo */
    .ribbon {
      position: absolute;
      bottom: 20px;
      width: 30px;
      height: 120px;
      background: #81b29a;
      border-radius: 10px;
      transform-origin: bottom center;
      opacity: 0;
      transition: all 0.8s ease;
      z-index: 1;
    }

    .ribbon-bow {
      position: absolute;
      bottom: 60px;
      width: 50px;
      height: 20px;
      background: #e63946;
      border-radius: 10px;
      z-index: 3;
      opacity: 0;
      transform: scale(0);
      transition: all 0.5s ease 1.2s;
    }

    .bouquet-container.active .ribbon {
      opacity: 1;
    }

    .bouquet-container.active .ribbon-bow {
      opacity: 1;
      transform: scale(1);
    }

    /* Flor individual */
    .flower {
      position: absolute;
      bottom: 100px;
      width: 80px;
      height: 80px;
      opacity: 0;
      transform: scale(0) translateY(50px);
      transition: all 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    }

    /* Animación al activar */
    .bouquet-container.active .flower {
      opacity: 1;
      transform: scale(1) translateY(0);
    }

    /* Posiciones del Ramo */
    .f1 { left: 100px; bottom: 140px; transition-delay: 0.2s; z-index: 2; }
    .f2 { left: 40px;  bottom: 110px; transition-delay: 0.4s; z-index: 2; transform: rotate(-20deg) scale(0); }
    .f3 { left: 160px; bottom: 110px; transition-delay: 0.6s; z-index: 2; transform: rotate(20deg) scale(0); }
    .f4 { left: 70px;  bottom: 170px; transition-delay: 0.8s; z-index: 2; }
    .f5 { left: 130px; bottom: 170px; transition-delay: 1.0s; z-index: 2; }

    .bouquet-container.active .f2 { transform: rotate(-20deg) scale(1) translateY(0); }
    .bouquet-container.active .f3 { transform: rotate(20deg) scale(1) translateY(0); }

    /* Partes de la Flor */
    .petals {
      position: relative;
      width: 100%;
      height: 100%;
      animation: rotateFlower 20s linear infinite;
    }

    .petal {
      position: absolute;
      top: 50%;
      left: 50%;
      width: 25px;
      height: 40px;
      background-color: #ffda3d;
      border-radius: 50% 50% 50% 50% / 80% 80% 20% 20%;
      transform-origin: top center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    .petal:nth-child(1) { transform: translate(-50%, 0) rotate(0deg); }
    .petal:nth-child(2) { transform: translate(-50%, 0) rotate(45deg); }
    .petal:nth-child(3) { transform: translate(-50%, 0) rotate(90deg); }
    .petal:nth-child(4) { transform: translate(-50%, 0) rotate(135deg); }
    .petal:nth-child(5) { transform: translate(-50%, 0) rotate(180deg); }
    .petal:nth-child(6) { transform: translate(-50%, 0) rotate(225deg); }
    .petal:nth-child(7) { transform: translate(-50%, 0) rotate(270deg); }
    .petal:nth-child(8) { transform: translate(-50%, 0) rotate(315deg); }

    .center {
      position: absolute;
      top: 50%;
      left: 50%;
      width: 24px;
      height: 24px;
      background-color: #8b5e3c;
      border-radius: 50%;
      transform: translate(-50%, -50%);
      z-index: 10;
      box-shadow: inset 0 0 4px rgba(0,0,0,0.3);
    }

    @keyframes rotateFlower {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
  </style>
</head>
<body>

  <div class="container">
    <h1 id="title">¡Tengo una sorpresa para ti! ✨</h1>
    
    <button id="btn" onclick="mostrarFlores()">Presiona aquí ❤️</button>

    <div class="bouquet-container" id="bouquet">
      <div class="ribbon"></div>
      <div class="ribbon-bow"></div>

      <!-- Flor 1 -->
      <div class="flower f1">
        <div class="petals">
          <div class="petal"></div><div class="petal"></div><div class="petal"></div><div class="petal"></div>
          <div class="petal"></div><div class="petal"></div><div class="petal"></div><div class="petal"></div>
        </div>
        <div class="center"></div>
      </div>

      <!-- Flor 2 -->
      <div class="flower f2">
        <div class="petals">
          <div class="petal"></div><div class="petal"></div><div class="petal"></div><div class="petal"></div>
          <div class="petal"></div><div class="petal"></div><div class="petal"></div><div class="petal"></div>
        </div>
        <div class="center"></div>
      </div>

      <!-- Flor 3 -->
      <div class="flower f3">
        <div class="petals">
          <div class="petal"></div><div class="petal"></div><div class="petal"></div><div class="petal"></div>
          <div class="petal"></div><div class="petal"></div><div class="petal"></div><div class="petal"></div>
        </div>
        <div class="center"></div>
      </div>

      <!-- Flor 4 -->
      <div class="flower f4">
        <div class="petals">
          <div class="petal"></div><div class="petal"></div><div class="petal"></div><div class="petal"></div>
          <div class="petal"></div><div class="petal"></div><div class="petal"></div><div class="petal"></div>
        </div>
        <div class="center"></div>
      </div>

      <!-- Flor 5 -->
      <div class="flower f5">
        <div class="petals">
          <div class="petal"></div><div class="petal"></div><div class="petal"></div><div class="petal"></div>
          <div class="petal"></div><div class="petal"></div><div class="petal"></div><div class="petal"></div>
        </div>
        <div class="center"></div>
      </div>
    </div>

    <div class="message" id="message">para tí mi niña 🌻💛</div>
  </div>

  <script>
    function mostrarFlores() {
      // Ocultar botón y título suavemente
      document.getElementById('btn').style.display = 'none';
      document.getElementById('title').innerText = ' Feliz 21 de Septiembre ';

      // Activar la animación del ramo de flores
      document.getElementById('bouquet').classList.add('active');

      // Mostrar el mensaje con un pequeño retraso
      setTimeout(() => {
        document.getElementById('message').classList.add('show');
      }, 1400);
    }
  </script>

</body>
</html>
