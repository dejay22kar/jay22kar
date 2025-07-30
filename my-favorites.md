
<body>
<div class="section">
  <button onclick="toggleSection(this)">🎵 My playlists</button>
  <div class="preview">The place I lived for 2 years in Sweden</div>
  <div class="content hidden">
    <p>
      <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/4gHX9noYu623xl5I2AWEaa?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
   </p>
  </div>
</div>

<div class="section">
  <button onclick="toggleSection(this)">📚 Literature</button>
  <div class="preview">Miscellaneous photos from India. Coming soon...</div>
  <div class="content hidden">
    
## A test
- _Harry Potter & Goblet of fire_ by J.K Rowling
- _Harry Potter & the Half-blood prince_ by J.K Rowling
- _Harry Potter & the Deathly hallows_ by J.K Rowling
   
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

  <script
    type="text/javascript"
    async defer
    src="//assets.pinterest.com/js/pinit.js"
></script>
  
  </body>
