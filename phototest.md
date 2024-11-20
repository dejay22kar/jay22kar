<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Photo Gallery</title>
  <style>
    /* Style for the grid layout */
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
      gap: 10px;
      padding: 20px;
    }
    .gallery img {
      width: 100%;
      height: auto;
      cursor: pointer;
      border-radius: 5px;
      transition: transform 0.3s ease;
    }
    .gallery img:hover {
      transform: scale(1.05);
    }

    /* Modal styles */
    .modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }
    .modal img {
      max-width: 80%;
      max-height: 80%;
      border-radius: 5px;
    }
    .modal .caption {
      color: white;
      margin-top: 10px;
      text-align: center;
      font-size: 18px;
    }
    .modal .close {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 30px;
      color: white;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1 style="text-align: center;">Photo Gallery</h1>

  <!-- Photo Grid -->
  <div class="gallery">
    <img src="https://images.pexels.com/photos/3680219/pexels-photo-3680219.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500" alt="Photo 1" data-caption="This is the description for Photo 1">
    <img src="https://posterjack.ca/cdn/shop/articles/Tips_for_Taking_Photos_at_the_Beach_55dd7d25-11df-4acf-844f-a5b4ebeff4df.jpg?v=1563409972&width=1500" alt="Photo 2" data-caption="This is the description for Photo 2">
    <img src="https://next-images.123rf.com/index/_next/image/?url=https://assets-cdn.123rf.com/index/static/assets/top-section-bg.jpeg&w=3840&q=75" alt="Photo 3" data-caption="This is the description for Photo 3">
    <img src="images/gothenburg/IMG_2520.heic" alt="Photo 4" data-caption="This is the description for Photo 4">
    <!-- Add more photos as needed -->
  </div>

  <!-- Modal -->
  <div class="modal" id="photoModal">
    <span class="close" onclick="closeModal()">&times;</span>
    <img id="modalImg" src="" alt="">
    <div class="caption" id="modalCaption"></div>
  </div>

  <script>
    // Get modal elements
    const modal = document.getElementById('photoModal');
    const modalImg = document.getElementById('modalImg');
    const modalCaption = document.getElementById('modalCaption');

    // Function to open the modal
    function openModal(img) {
      modal.style.display = 'flex';
      modalImg.src = img.src;
      modalCaption.textContent = img.getAttribute('data-caption');
    }

    // Function to close the modal
    function closeModal() {
      modal.style.display = 'none';
    }

    // Add click event to all images in the gallery
    document.querySelectorAll('.gallery img').forEach(img => {
      img.addEventListener('click', () => openModal(img));
    });
  </script>
</body>
</html>
