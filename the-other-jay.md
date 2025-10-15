
Well, I don't have a split personality disorder (or not that I'm aware of) and that you'd find my another personality over here.    

All I needed was just another place where I could have collection of some of my other writings which I am not comfortable with sharing with everyone *yet*, but I know I will be with my closed ones and a few others, and hence such a page with such a filter. The source of these writings were majorly from the difficult times and emotions that I have had in my life, and words - I think, I have felt to be the fastest and easiest way to express, validate and paint them.    

I intend to make them public in future but not so soon. But if you're curious — or for any reason would like to read them — feel free to reach out. I might be open to sharing if it feels like the right fit.



<html>
<head>
<style>
body {
  background-color: white;
  color: black;
}

/* Dark mode animation — only applied when body gets class */
body.dark-mode {
  animation-name: fadeToDark;
  animation-duration: 10s;
  animation-fill-mode: forwards;
}

@keyframes fadeToDark {
  from { background-color: white; color: black; }
  to { background-color: #202124; color: #E8E6E3; }
}
</style>
</head>

<body>
  <div style="text-align: center; padding: 20px; font-size: 24px;">
    Password:
    <input type="password" id="passwordInput" placeholder="Enter password"
      style="font-size: 20px; text-align: center; background-color: black; color: white; border: 1px solid black; outline: none; caret-color: white;">
    <button onclick="checkPassword()">Submit</button>
  </div>

<div id="secretGIF" style="display: none; text-align: center; margin-top: 20px;">
  <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; margin: auto;">
    <iframe src="https://tenor.com/embed/19918388"
            style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
            frameborder="0"
            allowfullscreen>
    </iframe>
  </div>
</div>

<script>
function checkPassword() {
    const password = document.getElementById("passwordInput").value;
    const correctPassword = "jay222kar"; // replace with your actual password

    if (password === correctPassword) {
        // Add the class to trigger animation
        document.body.classList.add("dark-mode");

        // Show the GIF
        document.getElementById("secretGIF").style.display = "block";

        // Redirect after 10 seconds
        setTimeout(function() {
            window.location.href = "https://jay22kar.me/the-other-jay/"; 
        }, 8000);
    } else {
        alert("Incorrect password. Please try again.");
    }
}
</script>
</body>
</html>
