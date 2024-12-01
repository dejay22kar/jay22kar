# My Photo Gallery

Welcome to my photo gallery! Click on any image to see the full size.


<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Image Gallery</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightgallery/2.7.1/css/lightgallery.min.css">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/lightgallery/2.7.1/lightgallery.min.js"></script>
</head>
<body>
  <h1>My Photo Gallery</h1>
  <div id="lightgallery">
    <a href="https://img.freepik.com/free-photo/colorful-design-with-spiral-design_188544-9588.jpg">
      <img src="https://img.freepik.com/free-photo/colorful-design-with-spiral-design_188544-9588.jpg" alt="Image 1" style="width: 150px;">
    </a>
    <a href="https://th.bing.com/th/id/OIG3.80EN2JPNx7kp5VqoB5kz">
      <img src="https://th.bing.com/th/id/OIG3.80EN2JPNx7kp5VqoB5kz" alt="Image 2" style="width: 150px;">
    </a>
    <a href="https://img.freepik.com/free-photo/colorful-design-with-spiral-design_188544-9588.jpg">
      <img src="https://img.freepik.com/free-photo/colorful-design-with-spiral-design_188544-9588.jpg" alt="Image 3" style="width: 150px;">
    </a>
    <!-- Add more images -->
  </div>
  <script>

Yes, you can prevent the "download" option in LightGallery and make it harder for users to save images. While you can't completely prevent determined users from saving images (e.g., taking screenshots), you can implement measures to discourage it.

Disable the Download Option
LightGallery provides an option to disable the "download" button in the settings. Here's how you can do it:

Updated Code:
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Image Gallery</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightgallery/2.7.1/css/lightgallery.min.css">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/lightgallery/2.7.1/lightgallery.min.js"></script>
</head>
<body>
  <h1>My Photo Gallery</h1>
  <div id="lightgallery">
    <a href="https://i.imgur.com/yourimage1.jpg">
      <img src="https://i.imgur.com/yourimage1.jpg" alt="Image 1" style="width: 150px;">
    </a>
    <a href="https://i.imgur.com/yourimage2.jpg">
      <img src="https://i.imgur.com/yourimage2.jpg" alt="Image 2" style="width: 150px;">
    </a>
    <a href="https://i.imgur.com/yourimage3.jpg">
      <img src="https://i.imgur.com/yourimage3.jpg" alt="Image 3" style="width: 150px;">
    </a>
    <!-- Add more images -->
  </div>
  <script>
    lightGallery(document.getElementById('lightgallery'), {
      plugins: [lgZoom, lgThumbnail], // Use zoom and thumbnail plugins
      download: false // Disable the download button
  </script>
</body>
</html>
