
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Homepage with Background Video</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    .video-background {
      position: fixed;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      z-index: -1;
      overflow: hidden;
    }

    .video-background video {
      width: 100%;
      height: 100%;
      object-fit: cover;
      opacity: 0.6; /* Adjust this to control video brightness */
    }

body, html {
  height: 100%;
  margin: 0;
  padding: 0;
  font-family: sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
}

.menu-box {
  background-color: rgba(255, 255, 255, 0.85);
  padding: 40px 60px;
  border-radius: 30px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
  text-align: center;
  min-width: 300px;
  max-width: 90%;
  width: 300px;
}

    .menu-box h1 {
      margin-bottom: 20px;
      font-size: 24px;
    }

    .menu-box a {
      display: block;
      margin: 10px 0;
      padding: 12px 20px;
      background-color: #444;
      color: white;
      border-radius: 15px;
      text-decoration: none;
      font-size: 18px;
      transition: background 0.3s;
    }

    .menu-box a:hover {
      background-color: #666;
    }
  </style>
</head>
<body>

  <!-- Background video container -->
  <div class="video-background">
    <video autoplay loop muted playsinline preload="auto">
      <source src="photos/Timeline 1.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>

  <!-- Menu Box -->
  <div class="menu-box">
    <a href="music.html">🎵 Music</a>
    <a href="about.html">👤 About Me</a>
    <a href="photos.html">💭 Photos</a>
    <a href="thoughts.html">💭 Thoughts</a>
  </div>

</body>
</html>


## [Thoughts](https://dejay22kar.github.io/jay22kar/thoughts) | [Writing](https://dejay22kar.github.io/jay22kar/flash-fiction-and-short-stories) | [Music](https://dejay22kar.github.io/jay22kar/my-favorite-music) | [Games](https://dejay22kar.github.io/jay22kar/games) | [The other Jay](https://dejay22kar.github.io/jay22kar/jay222kar)

