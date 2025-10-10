<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Night Sky with Twinkling Stars</title>
<style>
  body {
    margin: 0;
    background: #0f2733; /* your color */
    overflow: hidden;
  }
  canvas {
    position: fixed;
    top: 0;
    left: 0;
  }
</style>
</head>
<body>
<canvas id="stars"></canvas>

<script>
const canvas = document.getElementById("stars");
const ctx = canvas.getContext("2d");
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

// Adjust this number for density of stars
const stars = Array.from({ length: 250 }, () => ({
  x: Math.random() * canvas.width,
  y: Math.random() * canvas.height,
  r: Math.random() * 1.5 + 0.5,
  o: Math.random()
}));

function drawMoon() {
  const x = canvas.width - 100;
  const y = 100;
  const radius = 40;

  const gradient = ctx.createRadialGradient(x, y, radius * 0.5, x, y, radius * 2);
  gradient.addColorStop(0, "rgba(255, 255, 210, 0.8)");
  gradient.addColorStop(1, "rgba(255, 255, 210, 0)");

  ctx.fillStyle = gradient;
  ctx.beginPath();
  ctx.arc(x, y, radius * 2, 0, Math.PI * 2);
  ctx.fill();

  ctx.fillStyle = "#fefcd7";
  ctx.beginPath();
  ctx.arc(x, y, radius, 0, Math.PI * 2);
  ctx.fill();
}

function drawStars() {
  ctx.fillStyle = "#0f2733"; // clear with background
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  // draw twinkling stars
  ctx.fillStyle = "white";
  stars.forEach(star => {
    ctx.globalAlpha = star.o;
    ctx.beginPath();
    ctx.arc(star.x, star.y, star.r, 0, Math.PI * 2);
    ctx.fill();
    // control twinkling speed here ↓↓↓
    star.o += (Math.random() - 0.5) * 0.05; 
    if (star.o < 0.1) star.o = 0.1;
    if (star.o > 1) star.o = 1;
  });

  // draw glowing moon
  drawMoon();

  requestAnimationFrame(drawStars);
}

drawStars();
</script>
</body>
</html>
