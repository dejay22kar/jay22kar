#Photos
Here are a bunch of photos I have taken.

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Image Gallery</title>
  <style>
    img {
      height: auto; /* Maintain aspect ratio */
      pointer-events: none;
    }
  </style>
</head>
<body>
  <!-- Your Image Gallery -->
<div id="cphgallery">
  <a href="photos/copenhagen/cph_1.webp">
    <img src="photos/copenhagen/cph_1.webp" alt="Copenhagen_image_1">
  </a>
  <a href="photos/copenhagen/cph_2.webp">
    <img src="photos/copenhagen/cph_2.webp" alt="Copenhagen_image_2">
  </a>
    <a href="photos/copenhagen/cph_6.webp">
    <img src="photos/copenhagen/cph_6.webp" alt="Copenhagen_image_1">
  </a>
  <a href="photos/copenhagen/cph_12.webp">
    <img src="photos/copenhagen/cph_12.webp" alt="Copenhagen_image_2">
  </a>
</div>
  <!-- JavaScript -->
  <script>
    document.querySelectorAll('img').forEach((img) => {
      img.onload = () => {
        if (img.naturalWidth > img.naturalHeight) {
          // Landscape
          img.style.width = '250px';
        } else {
          // Portrait
          img.style.width = '150px';
        }
      };
    });
  </script>
  
  <script>
    lightGallery(document.getElementById('cphgallery'), {
       
      download: false 
        });
  </script>
</body>
</html>
