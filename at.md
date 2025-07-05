# hello
Just testing

<div id="typewriter">
  <p id="typed text"></p>
</div>

<script>
  const text = `It was November 2024 and it randomly came upto me and it suddenly struck to me ‘Damn… 2025 is already here. I’ve been through sooo much this year, I wonder if I could put it one line?’. Then I was curious how many years can I describe in one line and here we go`;
  const speed = 20; // typing speed in milliseconds
  let i = 0;

  function typeWriter() {
    if (i < text.length) {
      document.getElementById("typed-text").innerHTML += text.charAt(i);
      i++;
      setTimeout(typeWriter, speed);
    }
  }

  window.onload = typeWriter;
</script>



