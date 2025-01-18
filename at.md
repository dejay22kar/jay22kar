# hello
Just testing
1

<svg width="500" height="200" xmlns="http://www.w3.org/2000/svg">
  <path
    d="M10 80 C 40 10, 65 10, 95 80 S 150 150, 180 80"
    stroke="black"
    fill="transparent"
    stroke-width="2"
    stroke-linecap="round"
    stroke-dasharray="300"
    stroke-dashoffset="300"
    id="animatedPath"
  />
</svg>

<style>
  #animatedPath {
    animation: draw 2s linear forwards;
  }

  @keyframes draw {
    to {
      stroke-dashoffset: 0;
    }
  }
</style>

# 2
<svg width="500" height="200" xmlns="http://www.w3.org/2000/svg">
  <path
    d="M10 80 C 40 10, 65 10, 95 80 S 150 150, 180 80"
    stroke="black"
    fill="transparent"
    stroke-width="2"
    id="motionPath"
  />
  <circle cx="0" cy="0" r="5" fill="red">
    <animateMotion dur="3s" repeatCount="indefinite">
      <mpath href="#motionPath" />
    </animateMotion>
  </circle>
</svg>

# 3
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 500 200">
  <path
    id="motionPath"
    d="M10 80 C 40 10, 65 10, 95 80 S 150 150, 180 80"
    stroke="black"
    fill="transparent"
    stroke-width="2"
  />
</svg>
<div class="circle"></div>

<style>
  .circle {
    width: 20px;
    height: 20px;
    background-color: red;
    border-radius: 50%;
    position: absolute;
    animation: moveAlongPath 3s linear infinite;
    offset-path: path("M10 80 C 40 10, 65 10, 95 80 S 150 150, 180 80");
  }

  @keyframes moveAlongPath {
    0% {
      offset-distance: 0%;
    }
    100% {
      offset-distance: 100%;
    }
  }
</style>

