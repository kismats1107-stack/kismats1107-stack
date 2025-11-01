<canvas id="stars"></canvas>
<script>
const canvas = document.getElementById('stars');
const ctx = canvas.getContext('2d');
canvas.width = innerWidth; canvas.height = innerHeight;

const stars = Array.from({length: 50}, () => ({
  x: Math.random()*canvas.width,
  y: Math.random()*canvas.height,
  size: Math.random()*2,
  speed: Math.random()*2 + 0.5
}));

function animate() {
  ctx.fillStyle = "rgba(0,0,20,0.2)";
  ctx.fillRect(0,0,canvas.width,canvas.height);
  for (let s of stars) {
    s.x -= s.speed;
    s.y += s.speed;
    if (s.x < 0 || s.y > canvas.height) {
      s.x = Math.random()*canvas.width;
      s.y = 0;
    }
    ctx.beginPath();
    ctx.arc(s.x, s.y, s.size, 0, Math.PI*2);
    ctx.fillStyle = "white";
    ctx.fill();
  }
  requestAnimationFrame(animate);
}
animate();
</script>
