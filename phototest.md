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


   ## Copenhagen
  <div id="cphgallery">
<a href="photos/copenhagen/cph_1.webp">
  <img src="photos/copenhagen/cph_1.webp" alt="A random building" style="width: 150px;">
</a>
<a href="photos/copenhagen/cph_2.webp">
  <img src="photos/copenhagen/cph_2.webp" alt="Darkness... is the new normal!" style="width: 150px;">
</a>
<a href="photos/copenhagen/cph_3.webp">
  <img src="photos/copenhagen/cph_3.webp" alt="Copenhagen_image_3" style="width: 150px;">
</a>
    <a href="https://th.bing.com/th/id/OIG3.80EN2JPNx7kp5VqoB5kz">
      <img src="https://th.bing.com/th/id/OIG3.80EN2JPNx7kp5VqoB5kz" alt="Image 2" style="width: 150px;">
    </a>
    <a href="https://img.freepik.com/free-photo/colorful-design-with-spiral-design_188544-9588.jpg">
      <img src="https://img.freepik.com/free-photo/colorful-design-with-spiral-design_188544-9588.jpg" alt="Image 3" style="width: 150px;">
    </a>
    <!-- Add more images -->
  </div>
  
  <style>
  img {
pointer-events: none;
  }
 </style>
  
  <script>
    lightGallery(document.getElementById('cphgallery'), {
       
      download: false 
        });
  </script>
</body>
