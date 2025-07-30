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
      margin: 1em auto;
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
  <p>This is the first part of the article...</p>

  <div class="hidden-content" style="display: none;">
    <p>Details revealed after clicking first button.</p>
  </div>

  <button class="show-more-btn">I wanna know more...</button>
</div>

  <div class="hidden-content" style="display: none;">
    <p>2nd SHOW MORE AS A TEST</p>
  </div>

  <button class="show-more-btn" style="display: none;">A little more...</button>
</div>

  <div class="hidden-content" style="display: none;">
    <p>3RD SHOW MORE AS A TEST</p>
  </div>

  <button class="show-more-btn" style="display: none;">MORE!!</button>
</div>

<script>
  const buttons = document.querySelectorAll('.show-more-btn');

  buttons.forEach((button, index) => {
    button.addEventListener('click', () => {
      const section = button.closest('.content-section');
      const hidden = section.querySelector('.hidden-content');

      hidden.style.display = 'block';
      button.style.display = 'none';

      // Show the next button, if it exists
      const nextButton = buttons[index + 1];
      if (nextButton) {
        nextButton.style.display = 'inline-block';
      }
    });
  });
</script>


</body>
</html>
