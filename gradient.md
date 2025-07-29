<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gradient Test</title>
  <style>
    html, body {
      height: 100%;
      margin: 0;
      font-family: 'Nunito', sans-serif;
    }

    body {
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(-45deg, #ffffff, #b3d9ff, #d5b8ff, #c0f0e8);
      background-size: 400% 400%;
      animation: animatedGradient 30s ease infinite;
      transition: background 1s ease;
    }

    @keyframes animatedGradient {
      0% {
        background-position: 0% 50%;
      }
      50% {
        background-position: 100% 50%;
      }
      100% {
        background-position: 0% 50%;
      }
    }

    .menu-box {
      background-color: rgba(255, 255, 255, 0.85);
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 0 25px rgba(0, 0, 0, 0.3);
      width: 80%;
      max-width: 300px;
    }
  </style>
</head>
<body>
  <div class="menu-box">
    <h1>Hello!</h1>
    <p>This is a gradient background test.</p>
  </div>
</body>
</html>
