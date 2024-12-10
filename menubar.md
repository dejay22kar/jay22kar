<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Menu Bar</title>
  <style>
    /* Basic styling for the body */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }

    /* Styling for the navigation bar */
    .navbar {
      background-color: #333; /* Dark background */
      overflow: hidden; /* Clear floats */
      display: flex; /* Flex layout */
      justify-content: space-between; /* Space between logo and menu */
      align-items: center; /* Center items vertically */
      padding: 10px 20px;
    }

    /* Navigation links */
    .navbar a {
      color: white; /* White text */
      text-decoration: none; /* Remove underline */
      padding: 10px 20px;
    }

    /* Hover effect for links */
    .navbar a:hover {
      background-color: #575757; /* Gray background on hover */
    }

    /* Hamburger menu icon */
    .hamburger {
      display: none; /* Hidden by default */
      font-size: 24px;
      color: white;
      cursor: pointer;
    }

    /* Dropdown menu */
    .menu {
      display: flex; /* Show menu items side by side */
    }

    /* Responsive design */
    @media screen and (max-width: 600px) {
      .menu {
        display: none; /* Hide menu by default on small screens */
        flex-direction: column; /* Stack links vertically */
        background-color: #333; /* Same background as navbar */
        width: 100%; /* Full width */
        position: absolute; /* Absolute positioning */
        top: 50px; /* Below the navbar */
        left: 0;
      }

      .menu.show {
        display: flex; /* Show menu when toggled */
      }

      .hamburger {
        display: block; /* Show hamburger on small screens */
      }
    }
  </style>
</head>
<body>
  <!-- Navigation Bar -->
  <div class="navbar">
    <div class="logo">
      <a href="#home" style="font-size: 24px; font-weight: bold;">MySite</a>
    </div>
    <div class="hamburger" id="hamburger">&#9776;</div>
    <div class="menu" id="menu">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#gallery">Gallery</a>
      <a href="#contact">Contact</a>
    </div>
  </div>

  <!-- Page Content -->
  <div style="padding: 20px;">
    <h1>Welcome to My Website</h1>
    <p>This is an example of a webpage with a responsive navigation bar.</p>
  </div>

  <script>
    // Toggle menu on hamburger click
    const hamburger = document.getElementById('hamburger');
    const menu = document.getElementById('menu');

    hamburger.addEventListener('click', () => {
      menu.classList.toggle('show');
    });
  </script>
</body>
</html>
