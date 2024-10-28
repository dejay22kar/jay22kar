## [Thoughts](https://dejay22kar.github.io/jay22kar/thoughts) | [Music](https://dejay22kar.github.io/jay22kar/music) | [Games](https://dejay22kar.github.io/jay22kar/games) | [The other Jay](https://dejay22kar.github.io/jay22kar/jay222kar)

<style>

body {
  background-color: white;
  color: black;
  animation-name: example;
  animation-duration: 10s;
  animation-delay: 2s;
  animation-fill-mode: forwards;
}
  @keyframes example {
  from {background-color: white;}
  to {background-color: #333333;}
  from {color: black;}
  to {color: white;}
}
</style>


<div style="text-align: center; background-color: black; color: white; padding: 20px; font-size: 24px;">
    Password:
    <input type="password" id="passwordInput" placeholder="Enter password" style="font-size: 20px;">
    <button onclick="checkPassword()">Submit</button>
</div>

<div id="secretImage" style="display: none; text-align: center; margin-top: 20px;">
    <img src="[your-image-url.jpeg](https://thumb.ac-illust.com/5a/5ae562edae316872b39a1667b6f38e2f_t.jpeg)" alt="Secret Image" style="width: 300px;">
</div>

<script>
function checkPassword() {
    const password = document.getElementById("passwordInput").value;
    const correctPassword = "test123"; // replace with your actual password

    if (password === correctPassword) {
        document.getElementById("secretImage").style.display = "block";
    } else {
        alert("Incorrect password. Please try again.");
    }
}
</script>

