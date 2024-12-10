<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Website with Menu Bar</title>
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
      display: flex; /* Use flexbox for layout */
      padding: 0 10px;
    }

    /* Style for the navigation links */
    .navbar a {
      color: white; /* White text */
      text-decoration: none; /* Remove underline */
      padding: 14px 20px; /* Add some padding */
      display: block;
    }

    /* Hover effect for links */
    .navbar a:hover {
      background-color: #575757; /* Gray background on hover */
    }

    /* Add responsiveness: stack links on smaller screens */
    @media screen and (max-width: 600px) {
      .navbar {
        flex-direction: column; /* Stack the links vertically */
      }
    }
  </style>
</head>
<body>
  <!-- Menu Bar -->
  <div class="navbar">
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#gallery">Gallery</a>
    <a href="#contact">Contact</a>
  </div>

  <!-- Page Content -->
  <div style="padding: 20px;">
    <h1>Welcome to My Website</h1>
    <p>This is an example of a webpage with a simple menu bar.</p>
  </div>
</body>
</html>
