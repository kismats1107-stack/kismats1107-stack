<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Glowing Gradient | Kismat Shah</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(-45deg, #ff00c8, #00e0ff, #00ff6a, #ff9100);
      background-size: 400% 400%;
      animation: gradientShift 8s ease infinite;
      color: white;
      font-family: 'Orbitron', sans-serif;
      font-size: 2rem;
    }
    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }
  </style>
</head>
<body>
  👋 Hi, I'm <strong>Kismat Shah</strong> — CSE Explorer 🚀
</body>
</html>
