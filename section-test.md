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
    column-count: 5;
    column-gap: 10px;

  }
  .gallery img {
    width: 100%;
    display: block;
    margin-bottom: 10px;
  }
  img {
pointer-events: none;
  }
</style>

<div class="section">
  <button onclick="toggleSection(this)">Section 1</button>
  <div class="preview">This is a short preview of section 1...</div>
  <div class="content hidden">
    <p>This is the full content of Section 1. It could be a longer paragraph that only shows up when the section is expanded.</p>
  </div>
</div>

<div class="section">
  <button onclick="toggleSection(this)">Section 2</button>
  <div class="preview"> 
  A short teaser for section 2 goes here... 
  </div>
  <div class="content hidden">
    <p>This is the full content of Section 2. Again, this appears only when you click the button.
     And lemme try adding an image here.  
     Next line and now on the next one...  <img src="https://letsenhance.io/static/73136da51c245e80edc6ccfe44888a99/1015f/MainBefore.jpg" alt="Example" style="max-width: 100%; border-radius: 8px;"> 
    One more line just to check.
    </p>
  </div>
</div>

<div class="section">
  <button onclick="toggleSection(this)">Room 1514</button>
  <div class="preview">The place I lived for 2 years in Sweden</div>
  <div class="content hidden">
    <p>
      Here are some photos that I have taken in and from my room in Gothenburg, Sweden, over the time. I have had some of my worst and - I wouldn't say best - but the most meaningful times (and "metamorphosis stage) of my life in this house. Naturally, I have grown to be very fond and attached to it since it gave me a safe space to be and feel anything, anytime. It has been one of the best things that has happened to me and perhaps this is my humble way to capture it, to keep it with me, in the form of photos (and videos on YouTube). I will forever be grateful to universe for this house, this room - Room 1514.

<div class="gallery" id="roomGallery"></div>

<script>
  const galleryContainer = document.getElementById('roomGallery');
  const totalImages = 70; // Total number of images

  for (let i = 1; i <= totalImages; i++) {
    const link = document.createElement('a');
    link.href = `photos/room1514/room1514_${i}.webp`;

    const image = document.createElement('img');
    image.src = `photos/room1514/thumbnail_room1514_${i}.webp`;
    image.alt = `Room1514_image_${i}`;
    
    link.appendChild(image);
    galleryContainer.appendChild(link);
  }
</script>
    </p>
  </div>
</div>

<style>
.section {
  margin: 1.5em 0;
  padding: 1em;
  border: 1px solid #ffffff;
  border-radius: 10px;
  background-color: #ffffff;
}

button {
  font-size: 1.2em;
  font-weight: bold;
  padding: 0.5em 1em;
  cursor: pointer;
  background-color: #ffffff;
  border: 1px solid #888;
  border-radius: 5px;
  margin-bottom: 0.5em;
}

.preview {
  color: #444;
  margin-bottom: 0.5em;
  font-style: italic;
}

.content {
  margin-top: 0.5em;
}

.hidden {
  display: none;
}
</style>

<script>
function toggleSection(button) {
  const section = button.parentElement;
  const content = section.querySelector('.content');

  // Collapse all others
  document.querySelectorAll('.section .content').forEach(el => {
    if (el !== content) el.classList.add('hidden');
  });

  // Toggle this one
  content.classList.toggle('hidden');
}
</script>
