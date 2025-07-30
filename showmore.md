<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Read More Example</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 20px;
    }

    .content {
      line-height: 1.6;
      max-width: 600px;
      margin: 0 auto;
    }

    .hidden-content {
      display: none; /* Initially hide the bottom content */
    }

    .show-more-btn {
      display: block;
      margin: 20px auto;
      text-align: center;
      padding: 10px 20px;
      background-color: #007BFF;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
    }

    .show-more-btn:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>

<div class="content-section">
  <h1>My Long Article</h1>
  <p>This is the first part of the article...</p>
  <p>The reader can see this part immediately...</p>

  <div class="hidden-content" style="display: none;">
    <p>Now we delve into the details...</p>
    <p>Finally, we wrap up...</p>
  </div>
  <button class="show-more-btn">Show More</button>
</div>

<div class="content-section">
  <p>Another section...</p>
  <div class="hidden-content" style="display: none;">
    <p>2nd SHOW MORE AS A TEST</p>
  </div>
  <button class="show-more-btn">Show More</button>
</div>

<div class="content-section">
  <p>Yet another section...</p>
  <div class="hidden-content" style="display: none;">
    <p>3RD SHOW MORE AS A TEST</p>
  </div>
  <button class="show-more-btn">Show More</button>
</div>

<script>
  const buttons = document.querySelectorAll('.show-more-btn');

  buttons.forEach(button => {
    button.addEventListener('click', () => {
      const parent = button.closest('.content-section');
      const hidden = parent.querySelector('.hidden-content');

      hidden.style.display = 'block';
      button.style.display = 'none';
    });
  });
</script>

</body>
</html>
