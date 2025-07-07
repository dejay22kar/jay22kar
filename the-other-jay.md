## [Thoughts](https://dejay22kar.github.io/jay22kar/thoughts) | [Music](https://dejay22kar.github.io/jay22kar/music) | [Games](https://dejay22kar.github.io/jay22kar/games) | [The other Jay](https://dejay22kar.github.io/jay22kar/jay222kar)

Well, I don't have a split personality disorder (or not that I'm aware of🫢) and that you'd find my another personality over here. 
Here you would find yet just another recollection of some of my writings which I am not comfortable with sharing with everyone *yet*, but I would make them public in near future. These source of these writings were from majorly from the toughest times of my life and are related to mental health issues, trauma and toxic behaviors that we learn on our way to protect ourselves. 

Simply put, this page consists just another collection of my writings which I am not comfortable sharing with everyone *yet*. But I know I would be with some people and I needed a place where I can keep them all at one place. Hence, this page :)
If you're curious enough to want to read them, please contact me and then let me decide if I am comfortable enough with sharing you :)


<!DOCTYPE html>
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
    const correctPassword = "123"; // replace with your actual password

    if (password === correctPassword) {
        // Add the class to trigger animation
        document.body.classList.add("dark-mode");

        // Show the GIF
        document.getElementById("secretGIF").style.display = "block";

        // Redirect after 10 seconds
        setTimeout(function() {
            window.location.href = "https://mechstuff.com"; 
        }, 10000);
    } else {
        alert("Incorrect password. Please try again.");
    }
}
</script>
</body>
</html>
