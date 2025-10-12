<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Clair de lone – Night Sky</title>
<style>
  html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    color: white;
    font-family: sans-serif;
    overflow-x: hidden;
    background: none;
  }
  canvas {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
  }
  .content {
    max-width: 800px;
    margin: 60px auto;
    padding: 0 20px;
  }
  #fade-overlay {
    position: fixed;
    top: 0; left: 0;
    width: 100vw; height: 100vh;
    background: white;
    z-index: 9999;
    pointer-events: none;
    opacity: 1;
    transition: opacity 3s ease;
  }
</style>
</head>
<body>
  <div id="fade-overlay"></div>
  <canvas id="stars"></canvas>

  <div class="content">
    <h1 style="text-align: center;">Clair de lone</h1>
    <p>It was one of those long narrow streets and it was night.<br>
    I was alone, but not lone.</p>
    <p>All the wooden shops on both the sides were closed.<br>
    There was no source of light, except the moonlight.</p>
    <p>As I walked on that narrow street, I kept wanting to walk more.<br>
    But as I reached the end of the street, I looked back again and I could see only two colours - the darkness and the moonlight.</p>
    <p>I came back again to the centre, not wanting this moment to end.<br>
    As the rays of moonlight fell on the roofs, I could see the stardust vaporising off the surface towards the sky. It was all glittering, my dear friend.</p>
    <p>Was the stardust white? Or was it blue? It was white and blue.<br>
    Exactly like the moon and the moonlight - the moon bright white yet the moonlight seeming so blue.</p>
    <p>The mind inside the dream me, made that sparkling and twinkling sound.<br>
    “That’s how it sounds in the movies!”, thought the dream me.</p>
    <p>I saw myself in the centre of the street, my moonlit face, so blank and so awed,<br>
    as I saw this whole surreal, mystical land evaporating... except me, so odd.</p>
    <p>There were no people, as were no thoughts.<br>
    Forget thinking, I wasn’t even feeling - neither my breaths nor my feet on the ground, I was completely lost.</p>
    <p>I was not me.<br>
    I was those wooden shops, that cobbled street, that shimmering stardust, the moon and the moonlight and that is why I still know them so well.</p>
    <p>I was alone, but not lone.<br>
    I experienced Clair de lone.</p><br>
    
    <p><a href="https://dejay22kar.github.io/jay22kar/thoughts-and-feelings" style="color:#9dd6ff;">🠔 Back to Thoughts and Feelings</a></p>
  </div>

<script>
const canvas = document.getElementById("stars");
const ctx = canvas.getContext("2d");

function resizeCanvas() {
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
}
resizeCanvas();
window.addEventListener("resize", resizeCanvas);

const stars = Array.from({ length: 80 }, () => ({
  x: Math.random() * canvas.width,
  y: Math.random() * canvas.height,
  r: Math.random() * 1.5 + 0.5,
  o: Math.random(),
  speed: (Math.random() * 0.12) + 0.08
}));

let moonOpacity = 0;

// --- Moon Drawing ---
function drawMoon() {
  const x = canvas.width - 80;
  const y = 80;
  const radius = 22;

  const gradient = ctx.createRadialGradient(x, y, radius * 0.5, x, y, radius * 2);
  gradient.addColorStop(0, `rgba(255, 255, 210, ${0.5 * moonOpacity})`);
  gradient.addColorStop(1, `rgba(255, 255, 210, 0)`);
  ctx.fillStyle = gradient;
  ctx.beginPath();
  ctx.arc(x, y, radius * 2, 0, Math.PI * 2);
  ctx.fill();

  ctx.fillStyle = `rgba(254, 252, 215, ${moonOpacity})`;
  ctx.beginPath();
  ctx.arc(x, y, radius, 0, Math.PI * 2);
  ctx.fill();
}

// --- Shooting Star ---
let shootingStars = [];
const shootingStarAngle = 30 * Math.PI / 180; // 30° in radians
const starSpeed = 600; // pixels per second (adjust to taste)

function spawnShootingStar() {
  const startX = 0; // left edge
  const startY = canvas.height * 0.42; // about upper-center (adjust as needed)
  const vx = Math.cos(shootingStarAngle) * starSpeed; // x speed
  const vy = Math.sin(shootingStarAngle) * starSpeed; // y speed
  shootingStars.push({
    x: startX,
    y: startY,
    vx: vx,
    vy: vy,
    startTime: performance.now()
  });
}

function drawShootingStars(now) {
  for (let i = 0; i < shootingStars.length; i++) {
    let star = shootingStars[i];
    // Find how long this star has been alive
    let elapsed = (now - star.startTime) / 1000; // in seconds
    let currX = star.x + star.vx * elapsed;
    let currY = star.y + star.vy * elapsed;
    let tailX = currX - star.vx * 0.1; // 0.1 second behind
    let tailY = currY - star.vy * 0.1;

    // Remove stars if they're off-screen
    if (currX > canvas.width || currY > canvas.height) {
      shootingStars.splice(i, 1);
      i--;
      continue;
    }

    ctx.save();
    ctx.strokeStyle = "rgba(150,200,255,0.6)";
    ctx.lineWidth = 2;
    ctx.beginPath();
    ctx.moveTo(tailX, tailY);
    ctx.lineTo(currX, currY);
    ctx.stroke();
    ctx.restore();

    ctx.save();
    ctx.fillStyle = "white";
    ctx.beginPath();
    ctx.arc(currX, currY, 3, 0, Math.PI * 2);
    ctx.fill();
    ctx.restore();
  }
}

// In your animation loop, pass the current timestamp:
function drawStars(now) {
  ctx.fillStyle = "#0B1E44";
  ctx.fillRect(0, 0, canvas.width, canvas.height);
  // ... existing star/moon code ...
  drawShootingStars(now);
  requestAnimationFrame(drawStars);
}

// Launch a shooting star every 5 seconds
setInterval(spawnShootingStar, 5000);
// Kick off the loop
requestAnimationFrame(drawStars);
}

// --- Fade-in and animation start ---
window.addEventListener('load', () => {
  const overlay = document.getElementById('fade-overlay');
  overlay.style.opacity = '0';
  setTimeout(() => {
    overlay.style.display = 'none';
    const fadeDuration = 2000;
    const fadeStart = performance.now();

    function fadeMoon(timestamp) {
      let progress = (timestamp - fadeStart) / fadeDuration;
      moonOpacity = Math.min(1, progress);
      if (moonOpacity < 1) requestAnimationFrame(fadeMoon);
    }
    requestAnimationFrame(fadeMoon);
  }, 3000);
});

setInterval(spawnShootingStar, 5000);
drawStars();
</script>


</body>
</html>

