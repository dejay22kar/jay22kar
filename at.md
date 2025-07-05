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
  <button onclick="toggleSection(this)">Section 3</button>
  <div class="preview">Section 3 summary or lead-in...</div>
  <div class="content hidden">
    <p>This is the full content of Section 3.</p>
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
  font-size: 1.1em;
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
