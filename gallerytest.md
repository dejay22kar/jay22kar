<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Image Gallery</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightgallery/2.7.1/css/lightgallery.min.css">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/lightgallery/2.7.1/lightgallery.min.js"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightgallery/2.7.1/css/lg-fullscreen.min.css">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/lightgallery/2.7.1/plugins/lg-fullscreen.min.js"></script>

</head>

<body>

<style>
  .gallery {
    column-count: 4;
    column-gap: 15px;

  }
  .gallery img {
    width: 100%;
    display: block;
    margin-bottom: 15px;
  }
  img {
pointer-events: none;
  }
</style>

<h2> Copenhagen</h2> 

<div class="gallery" id="cphgallery">
  <a href="photos/copenhagen/cph_1.webp">
    <img src="photos/copenhagen/cph_1.webp" alt="Copenhagen_image_1">
  </a>
  <a href="photos/copenhagen/cph_2.webp">
    <img src="photos/copenhagen/cph_2.webp" alt="Copenhagen_image_2">
  </a>
  <a href="photos/copenhagen/cph_3.webp">
  <img src="photos/copenhagen/cph_3.webp" alt="Copenhagen_image_3"  />
</a>
<a href="photos/copenhagen/cph_4.webp">
  <img src="photos/copenhagen/cph_4.webp" alt="Copenhagen_image_4"  />
</a>
<a href="photos/copenhagen/cph_5.webp">
  <img src="photos/copenhagen/cph_5.webp" alt="Nyhaven"  />
</a>
<a href="photos/copenhagen/cph_6.webp">
  <img src="photos/copenhagen/cph_6.webp" alt="Church of Our Savior"  />
</a>
<a href="photos/copenhagen/cph_7.webp">
  <img src="photos/copenhagen/cph_7.webp" alt="City view from top of Church of Our Savior"  />
</a>
<a href="photos/copenhagen/cph_8.webp">
  <img src="photos/copenhagen/cph_8.webp" alt="Copenhagen_image_8"  />
</a>
<a href="photos/copenhagen/cph_9.webp">
  <img src="photos/copenhagen/cph_9.webp" alt="Copenhagen_image_9"  />
</a>
<a href="photos/copenhagen/cph_10.webp">
  <img src="photos/copenhagen/cph_10.webp" alt="Copenhagen_image_10"  />
</a>
<a href="photos/copenhagen/cph_11.webp">
  <img src="photos/copenhagen/cph_11.webp" alt="Copenhagen_image_11"  />
</a>
<a href="photos/copenhagen/cph_12.webp">
  <img src="photos/copenhagen/cph_12.webp" alt="Copenhagen_image_12"  />
</a>
<a href="photos/copenhagen/cph_13.webp">
  <img src="photos/copenhagen/cph_13.webp" alt="Copenhagen_image_13"  />
</a>
<a href="photos/copenhagen/cph_14.webp">
  <img src="photos/copenhagen/cph_14.webp" alt="Copenhagen_image_14"  />
</a>
<a href="photos/copenhagen/cph_15.webp">
  <img src="photos/copenhagen/cph_15.webp" alt="Copenhagen_image_15"  />
</a>
  <a href="photos/copenhagen/cph_16.webp">
  <img src="photos/copenhagen/cph_16.webp" alt="Copenhagen_image_16"  />
</a>
  <a href="photos/copenhagen/cph_17.webp">
  <img src="photos/copenhagen/cph_17.webp" alt="Copenhagen_image_17"  />
</a>
  <a href="photos/copenhagen/cph_18.webp">
  <img src="photos/copenhagen/cph_18.webp" alt="Copenhagen_image_18"  />
</a>
 <a>
   <img src="photos/copenhagen/cph_19.webp" alt="Copenhagen_image_19"  />
</a>
  <!-- More images -->
</div>

  <script>
    lightGallery(document.getElementById('cphgallery'), {
        download: false,        // Disable download button
        });

    const images = document.querySelectorAll('.gallery img');
    images.forEach(img => {
    img.addEventListener('contextmenu', (e) => e.preventDefault());
  });

    const links = document.querySelectorAll('.gallery a');
    links.forEach(link => {
    link.addEventListener('contextmenu', (e) => e.preventDefault());
    });
  </script>
  
  </body>
