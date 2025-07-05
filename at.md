<div class="section">
  <button onclick="toggleSection(this)">Section 1</button>
  <div class="content hidden">
    <p>This is the full content of Section 1.</p>
  </div>
</div>

<div class="section">
  <button onclick="toggleSection(this)">Section 2</button>
  <div class="content hidden">
    <p>This is the full content of Section 2.</p>
  </div>
</div>

<div class="section">
  <button onclick="toggleSection(this)">Section 3</button>
  <div class="content hidden">
    <p>This is the full content of Section 3.</p>
  </div>
</div>

<style>
.section {
  margin: 1em 0;
  padding: 1em;
  border: 1px solid #ccc;
  border-radius: 10px;
  background-color: #f9f9f9;
}

button {
  font-size: 1.2em;
  font-weight: bold;
  padding: 0.5em 1em;
  cursor: pointer;
  background-color: #fff;
  border: 1px solid #888;
  border-radius: 5px;
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

  // Collapse all other open sections
  document.querySelectorAll('.section .content').forEach(el => {
    if (el !== content) el.classList.add('hidden');
  });

  // Toggle current section
  content.classList.toggle('hidden');
}
</script>
