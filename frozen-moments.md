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
  <button onclick="toggleSection(this)">🇸🇪 Sweden</button>
  <div class="preview">Photos from Gothenburg, it's neighbouring islands and Stockholm</div>
  <div class="content hidden">
    <p>
      <div class="gallery" id="Sweden_Gallery"></div>

<script>
  var galleryContainer = document.getElementById('Sweden_Gallery');
  var totalImages = 37; // Total number of images

  for (let i = 1; i <= totalImages; i++) {
    const link = document.createElement('a');
    link.href = `photos/gothenburg/got_${i}.webp`;

    const image = document.createElement('img');
    image.src = `photos/gothenburg/thumbnail_got_${i}.webp`;
    image.alt = `Denmark_image_${i}`;
    
    link.appendChild(image);
    galleryContainer.appendChild(link);
  }
</script>
    </p>
  </div>
</div>

<div class="section">
  <button onclick="toggleSection(this)">🇩🇰 Denmark</button>
  <div class="preview"> 
  Photos from mere 4 days in Denmark
  </div>
  <div class="content hidden">
    <p>
      Most of the photos are from Copenhagen (Mother of God, I could talk about that city all day!) (The canals, the not-as-cold-as-Sweden and not-as-hot-as-Germany perfect temperature, the modern architecture but also containing European essence, the transporatation systems, the number of bicycles, the lush green parks in the very hearts of the city, the church bells and public naked pools - yes, you heard that right, my dear friend 🙃) (Also, Denmark is one of the highest paying countries in the world with an unmatched work-life balance.) (Wait, did I ever tell you about the time I met the prettiest girl I have ever-ever-ever talked to in my life here, in this city? Now, give me one good reason to not move there!) (Okay... I need to stop. I told you I could keep on going!). Som other photos are from Fredrikshavn and Skagen - the northern tip of Denmark. 
<div class="gallery" id="Copenhagen_Gallery"></div>

<script>
  var galleryContainer = document.getElementById('Copenhagen_Gallery');
  var totalImages = 23; // Total number of images

  for (let i = 1; i <= totalImages; i++) {
    const link = document.createElement('a');
    link.href = `photos/copenhagen/cph_${i}.webp`;

    const image = document.createElement('img');
    image.src = `photos/copenhagen/thumbnail_cph_${i}.webp`;
    image.alt = `Denmark_image_${i}`;
    
    link.appendChild(image);
    galleryContainer.appendChild(link);
  }
</script>
    </p>
  </div>
</div>

<div class="section">
  <button onclick="toggleSection(this)">🏡 Room 1514</button>
  <div class="preview">The place I lived for 2 years in Sweden</div>
  <div class="content hidden">
    <p>
      Here are some photos that I have taken in and from my room in Gothenburg, Sweden, over the time. I have had some of my worst and - I wouldn't say best - but the most meaningful times (and "metamorphosis" stage) of my life in this house. Naturally, I have grown to be very fond and attached to it since it gave me a safe space to be and feel anything, anytime. It has been one of the best things that has happened to me and perhaps this is my humble way to capture it, to keep it with me, in the form of photos (and videos on YouTube). I will forever be grateful to universe for this house, this room - Room 1514.

<div class="gallery" id="roomGallery"></div>

<script>
  var galleryContainer = document.getElementById('roomGallery');
  var totalImages = 74; // Total number of images

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

<div class="section">
  <button onclick="toggleSection(this)">🇵🇱 Poland</button>
  <div class="preview"> 
  Photos from my first solo trip to Poland for 9 days
  </div>
  <div class="content hidden">
    <p>
      It has been a month returning from Poland (while I write and upload these photos), and I would say it was... an experience. I am still processing what I felt and trying to give my feelings some words. Talking about the photos, I am a bit disappointed and unsatisfied because I expected I would have much more photos but apparently I don't. Nevermind, I know I am going to go back some day 🙂
<div class="gallery" id="Poland_Gallery"></div>

<script>
  var galleryContainer = document.getElementById('Poland_Gallery');
  var totalImages = 37; // Total number of images

  for (let i = 1; i <= totalImages; i++) {
    const link = document.createElement('a');
    link.href = `photos/poland/polska_${i}.webp`;

    const image = document.createElement('img');
    image.src = `photos/poland/thumbnail_polska_${i}.webp`;
    image.alt = `Polska_image_${i}`;
    
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

  <script>
  document.querySelectorAll('.gallery').forEach(gallery => {
  lightGallery(gallery, { download: false });
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

  <script
    type="text/javascript"
    async defer
    src="//assets.pinterest.com/js/pinit.js"
></script>
  
  </body>
