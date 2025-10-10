<canvas id="stars"></canvas>
<script>
  const canvas = document.getElementById("stars");
  const ctx = canvas.getContext("2d");
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;

  const stars = Array.from({ length: 200 }, () => ({
    x: Math.random() * canvas.width,
    y: Math.random() * canvas.height,
    r: Math.random() * 1.5,
    o: Math.random()
  }));

  function drawStars() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    ctx.fillStyle = "white";
    stars.forEach(star => {
      ctx.globalAlpha = star.o;
      ctx.beginPath();
      ctx.arc(star.x, star.y, star.r, 0, Math.PI * 2);
      ctx.fill();
      star.o += (Math.random() - 0.5) * 0.05;
      if (star.o < 0.1) star.o = 0.1;
      if (star.o > 1) star.o = 1;
    });
    requestAnimationFrame(drawStars);
  }
  drawStars();
</script>

<style>
  body {
    margin: 0;
    background: black;
    overflow: hidden;
  }
  canvas {
    position: fixed;
    top: 0;
    left: 0;
  }
</style>
