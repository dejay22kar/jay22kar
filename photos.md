#Photos
Here are a bunch of photos I have taken.

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Image Gallery</title>
  <style>
  .gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 10px; /* Space between images */
    justify-content: center; /* Center-align the grid */
  }

  /* Style each image */
  .gallery img {
    width: 100%;
    height: auto; /* Maintain aspect ratio */
  }
  </style>
</head>
<body>
  <!-- Your Image Gallery -->
<div id="cphgallery">
<a href="photos/copenhagen/cph_1.webp">
  <img src="photos/copenhagen/cph_1.webp" alt="A random building" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_2.webp">
  <img src="photos/copenhagen/cph_2.webp" alt="Darkness... is the new normal!" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_3.webp">
  <img src="photos/copenhagen/cph_3.webp" alt="Copenhagen_image_3" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_4.webp">
  <img src="photos/copenhagen/cph_4.webp" alt="Copenhagen_image_4" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_5.webp">
  <img src="photos/copenhagen/cph_5.webp" alt="Nyhaven" style="width: 250px;" />
</a>
<a href="photos/copenhagen/cph_6.webp">
  <img src="photos/copenhagen/cph_6.webp" alt="Church of Our Savior" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_7.webp">
  <img src="photos/copenhagen/cph_7.webp" alt="City view from top of Church of Our Savior" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_8.webp">
  <img src="photos/copenhagen/cph_8.webp" alt="Copenhagen_image_8" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_9.webp">
  <img src="photos/copenhagen/cph_9.webp" alt="Copenhagen_image_9" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_10.webp">
  <img src="photos/copenhagen/cph_10.webp" alt="Copenhagen_image_10" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_11.webp">
  <img src="photos/copenhagen/cph_11.webp" alt="Copenhagen_image_11" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_12.webp">
  <img src="photos/copenhagen/cph_12.webp" alt="Copenhagen_image_12" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_13.webp">
  <img src="photos/copenhagen/cph_13.webp" alt="Copenhagen_image_13" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_14.webp">
  <img src="photos/copenhagen/cph_14.webp" alt="Copenhagen_image_14" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_15.webp">
  <img src="photos/copenhagen/cph_15.webp" alt="Copenhagen_image_15" style="width: 150px;" />
</a>
<a href="photos/copenhagen/cph_16.webp">
  <img src="photos/copenhagen/cph_16.webp" alt="Copenhagen_image_16" style="width: 150px;" />
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
    }
    lightGallery(document.getElementById('cphgallery'), {
    download: false                                        
    });
  </script>
  
</body>
</html>
