
<body>
  <div class="section">
  <button onclick="toggleSection(this)">🎵 My playlists</button>
  <div class="preview"></div>
  <div class="content hidden">
    <p> Some of my favorite music - 
      <iframe data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/playlist/4gHX9noYu623xl5I2AWEaa?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
      <iframe data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/playlist/71DXTDsTlfXKgStgiwhFOA?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
      <iframe data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/playlist/1BrinBcOBDxL4HhqZnwrNP?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
   </p>
  </div>
</div>

<div class="section">
  <button onclick="toggleSection(this)">📚 Literature</button>
  <div class="preview"></div>
 <div class="content hidden">
     <p>Some books and short stories that I felt, understood or learned the most from - </p>
  <h2>Books</h2>
   <ul>
    <li><em>Harry Potter & Goblet of Fire</em> by J.K. Rowling</li>
    <li><em>Harry Potter & the Half-Blood Prince</em> by J.K. Rowling</li>
    <li><em>Harry Potter & the Deathly Hallows</em> by J.K. Rowling</li>
    <li><em>The Great Gatsby</em> by Scott Fitzgerald</li>
    <li><em>The Art of Strategy</em> by Dixit and Nalebuff</li>
    <li><em>Incognito</em> by David Eagleman</li>
    <li><em>The Power of Habit</em> by Charles Duhigg</li>
  </ul>

     <h2>Short stories</h2>
  <ul>
    <li><em>The hunger artist</em> by Franz Kafka</li>
    <li><em>The Swimmer</em> by John Cheever</li>
    <li><em>The most dangerous game</em> by Richard Connell</li>
    <li><em>How the leopard got his spots</em> by Rudyard Kipling</li>
  </ul>
</div>
</div>

<div class="section">
  <button onclick="toggleSection(this)">🎥 Films and TV series</button>
  <div class="preview"></div>
  <div class="content hidden">
      <p>And here are some of the my favorite movies and TV shows. Screen productions that provided me some value. Some of them offered incredible story, some goosebumps, some offered a punch at the end, some an edge of the seat thrill, some were just cinematic masterpieces - their camera movements, shots, transitions, an unprecedented way of showing stories visually, and some… just emotions - pure raw emotions which didn’t just touch me, it moved me to the bone and pierced through my heart through-and-through like a nice sharp and sleek Japanese katana sword.</p>

<h2 id="tv-shows">TV Shows</h2>
<ul>
  <li>Breaking Bad</li>
  <li>Game of Thrones (nope, not 8, there are only 7 seasons of GoT)</li>
  <li>The Last of Us</li>
  <li>Station Eleven</li>
  <li>Chernobyl</li>
  <li>Band of Brothers</li>
  <li>FRIENDS</li>
  <li>Modern family</li>
  <li>Normal people</li>
</ul>

<h2 id="animated">Animated</h2>
<ul>
  <li>Wall-E</li>
  <li>Big Hero 6</li>
  <li>Luca</li>
  <li>Despicable me</li>
  <li>Soul</li>
  <li>Coco</li>
  <li>Onward</li>
  <li>Inside Out</li>
  <li>Cars</li>
</ul>

<h2 id="bollywood">Bollywood</h2>
<ul>
  <li>Taare Zameen Par</li>
  <li>Highway</li>
  <li>Barfi!</li>
  <li>Talaash</li>
  <li>Ghajini</li>
  <li>Wake up Sid</li>
  <li>Masaan</li>
</ul>

<h2 id="hollywood-and-others">Hollywood and others</h2>
<ul>
  <li>Harry Potter series</li>
  <li>The Godfather trilogy</li>
  <li>The Batman trilogy</li>
  <li>The Before trilogy</li>
  <li>The Star wars prequel trilogy</li>
  <li>Amélie</li>
  <li>Past Lives</li>
  <li>Whiplash</li>
  <li>Her</li>
  <li>Lost in Translation</li>
  <li>Interstellar</li>
  <li>Inglorious Bastards</li>
  <li>Mr Bean Holidays</li>
  <li>La la land</li>
  <li>Schindler’s List</li>
  <li>The Imitation Game
… and so many more actually. I will add them as they strike me :)</li>
</ul>
  </div>
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
