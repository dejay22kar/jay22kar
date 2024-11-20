<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Photo Gallery</title>
  <style>
    /* Basic grid layout for the gallery */
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
      background-color: rgba(0, 0, 0, 0.9);
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }
    .modal img {
      max-width: 90%;
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

    /* Navigation arrows */
    .modal .arrow {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      font-size: 40px;
      color: white;
      cursor: pointer;
      user-select: none;
    }
    .modal .arrow.left {
      left: 10px;
    }
    .modal .arrow.right {
      right: 10px;
    }
  </style>
</head>
<body>
  <h1 style="text-align: center;">Photo Gallery</h1>

  <!-- Photo Grid -->
  <div class="gallery">
    <img src="photos/gothenburg/cdl.jpg" alt="Photo 1" data-index="0">
    <img src="photos/gothenburg/cdl.jpg" alt="Photo 2" data-index="1">
    <img src="photos/gothenburg/cdl.jpg" alt="Photo 3" data-index="2">
    <img src="photos/gothenburg/cdl.jpg" alt="Photo 4" data-index="3">
    <!-- Add more photos as needed -->
  </div>

  <!-- Modal -->
  <div class="modal" id="photoModal">
    <span class="close" onclick="closeModal()">&times;</span>
    <span class="arrow left" onclick="changeImage(-1)">&#10094;</span>
    <span class="arrow right" onclick="changeImage(1)">&#10095;</span>
    <img id="modalImg" src="" alt="">
    <div class="caption" id="modalCaption"></div>
  </div>

  <script>
    // Image gallery data
    const images = [
      { src: "photos/gothenburg/cdl.jpg", caption: "Photo 1 Description" },
      { src: "photos/gothenburg/IMG_2520.jpeg", caption: "Photo 2 Description" },
      { src: "photos/gothenburg/cdl.jpg", caption: "Photo 3 Description" },
      { src: "photos/gothenburg/IMG_2520.jpeg", caption: "Photo 4 Description" }
    ];

    // Modal elements
    const modal = document.getElementById("photoModal");
    const modalImg = document.getElementById("modalImg");
    const modalCaption = document.getElementById("modalCaption");
    let currentIndex = 0;

    // Open the modal
    function openModal(index) {
      currentIndex = index;
      modal.style.display = "flex";
      updateModal();
    }

    // Close the modal
    function closeModal() {
      modal.style.display = "none";
    }

    // Update modal content
    function updateModal() {
      modalImg.src = images[currentIndex].src;
      modalCaption.textContent = images[currentIndex].caption;
    }

    // Change image in modal
    function changeImage(direction) {
      currentIndex = (currentIndex + direction + images.length) % images.length;
      updateModal();
    }

    // Add click event to all images in the gallery
    document.querySelectorAll(".gallery img").forEach((img, index) => {
      img.addEventListener("click", () => openModal(index));
    });
  </script>
</body>
</html>
