<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Twinkling Night Sky</title>
<style>
  body {
    margin: 0;
    height: 100vh;
    background: black;
    overflow: hidden;
  }

  /* Create multiple layers of stars */
  .stars, .twinkling {
    position: absolute;
    width: 100%;
    height: 100%;
    display: block;
  }

  .stars {
    background: url('https://www.transparenttextures.com/patterns/stardust.png') repeat;
    z-index: 0;
  }

  .twinkling {
    background: transparent url('https://www.transparenttextures.com/patterns/stardust.png') repeat;
    animation: move-twinkling 200s linear infinite;
    opacity: 0.8;
    z-index: 1;
  }

  @keyframes move-twinkling {
    from {background-position: 0 0;}
    to {background-position: -10000px 5000px;}
  }

  /* Optional: overlay for your content */
  .content {
    position: relative;
    z-index: 2;
    color: white;
    text-align: center;
    padding-top: 40vh;
    font-size: 2rem;
  }
</style>
</head>
<body>
  <div class="stars"></div>
  <div class="twinkling"></div>
  <div class="content">⭐ Welcome to My Website ⭐</div>
</body>
</html>
