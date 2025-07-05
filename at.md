
<div class="accordion">
  <div class="section">
    <h2>Section 1</h2>
    <p class="preview">This is a short preview of section 1...</p>
    <div class="full-text hidden">
      <p>This is the full content of section 1.</p>
    </div>
    <button onclick="toggleSection(this)">Read more</button>
  </div>

  <div class="section">
    <h2>Section 2</h2>
    <p class="preview">Preview of section 2...</p>
    <div class="full-text hidden">
      <p>Here’s everything in section 2.</p>
    </div>
    <button onclick="toggleSection(this)">Read more</button>
  </div>

  <div class="section">
    <h2>Section 3</h2>
    <p class="preview">Section 3 starts here...</p>
    <div class="full-text hidden">
      <p>Details of section 3 go here.</p>
    </div>
    <button onclick="toggleSection(this)">Read more</button>
  </div>
</div>

.hidden {
  display: none;
}

.section {
  margin-bottom: 1.5em;
  padding: 1em;
  border-radius: 10px;
  background: #f2f2f2;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.section h2 {
  margin: 0 0 0.5em;
}

<script>
function toggleSection(button) {
  const section = button.closest('.section');
  const fullText = section.querySelector('.full-text');
  const allSections = document.querySelectorAll('.section');

  // Close all sections
  allSections.forEach(sec => {
    if (sec !== section) {
      sec.querySelector('.full-text').classList.add('hidden');
      sec.querySelector('button').textContent = 'Read more';
    }
  });

  // Toggle clicked section
  const isHidden = fullText.classList.contains('hidden');
  fullText.classList.toggle('hidden', !isHidden);
  button.textContent = isHidden ? 'Read less' : 'Read more';
}
</script>
