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

<div class="content">
  <h1>My Long Article</h1>
  <p>This is the first part of the article. It provides an introduction to the topic and engages the reader with some key points and an overview.</p>
  <p>The reader can see this part immediately, without needing to interact with the page. The content is concise and designed to pique interest.</p>
  
  <!-- Hidden content -->
  <div class="hidden-content" id="hiddenContent">
    <p>Now we delve into the details of the topic. This section provides in-depth information, examples, and analysis that expand upon the ideas introduced earlier</p>
    <p>Finally, we wrap up with conclusions, recommendations, and closing thoughts. This ensures the article has a comprehensive structure.</p>
  </div>  
  <!-- Show More Button -->
  <button class="show-more-btn" id="showMoreBtn">Show More</button>
</div>

  <!-- Hidden content -->
  <div class="hidden-content" id="hiddenContent">
    <p>2nd SHOW MORE AS A TEST</p>
  </div>
  <!-- Show More Button -->
  <button class="show-more-btn" id="showMoreBtn">Show More</button>
</div>

  <!-- Hidden content -->
  <div class="hidden-content" id="hiddenContent">
    <p>3RD SHOW MORE AS A TEST</p>
  </div>
  <!-- Show More Button -->
  <button class="show-more-btn" id="showMoreBtn">Show More</button>
</div>

<script>
  const showMoreBtn = document.getElementById('showMoreBtn');
  const hiddenContent = document.getElementById('hiddenContent');

  showMoreBtn.addEventListener('click', () => {
    hiddenContent.style.display = 'block'; // Show the hidden content
    showMoreBtn.style.display = 'none';   // Hide the "Show More" button
  });
</script>

</body>
</html>
