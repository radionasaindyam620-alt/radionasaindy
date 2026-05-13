<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Radio Ñasaindy en Vivo</title>

<style>
body{
  margin:0;
  font-family: Arial, sans-serif;
  background:#0b0b0b;
  color:white;
  display:flex;
  justify-content:center;
  align-items:center;
  height:100vh;
}

.player{
  background:#1a1a1a;
  padding:30px;
  border-radius:20px;
  text-align:center;
  width:320px;
  box-shadow:0 0 20px rgba(255,0,0,0.4);
}

.logo{
  width:100px;
  margin-bottom:10px;
}

.live{
  color:red;
  font-weight:bold;
  animation:blink 1s infinite;
}

@keyframes blink{
  50%{opacity:0.3;}
}

button{
  margin:10px 5px;
  padding:10px 15px;
  border:none;
  border-radius:10px;
  cursor:pointer;
  font-weight:bold;
}

.play{background:#ff0000;color:white;}
.pause{background:#333;color:white;}
</style>
</head>

<body>

<div class="player">

  <div class="live">🔴 EN VIVO</div>

  <!-- Logo (puedes cambiar la imagen) -->
  <img src="logo.png" class="logo" alt="Radio Ñasaindy">

  <h2>Radio Ñasaindy</h2>

  <audio id="radioPlayer">
    <source src="http://84.247.167.61:8000/stream?sid=1" type="audio/mpeg">
  </audio>

  <br>

  <button class="play" onclick="playRadio()">▶ Reproducir</button>
  <button class="pause" onclick="pauseRadio()">⏸ Pausar</button>

</div>

<script>
const radio = document.getElementById("radioPlayer");

function playRadio(){
  radio.play();
}

function pauseRadio(){
  radio.pause();
}
</script>

</body>
</html>
