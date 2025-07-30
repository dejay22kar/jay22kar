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

    .content-section {
  line-height: 1.6;
  max-width: 600px;
  margin: 0 auto 40px;
}

.button-wrapper {
  text-align: center;
  margin-top: 1em;
}

.show-more-btn {
  display: inline-block;
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
  <div class="hidden-content">
    <p>Details revealed after clicking first button.</p>
  </div>
  <div class="button-wrapper">
    <button class="show-more-btn">I wanna know more...</button>
  </div>
</div>

<div class="content-section">
  <p>Another interesting chunk...</p>
  <div class="hidden-content">
    <p>2nd SHOW MORE AS A TEST</p>
  </div>
  <div class="button-wrapper" style="display: none;">
    <button class="show-more-btn">A little more...</button>
  </div>
</div>

<div class="content-section">
  <p>Wrapping it up...</p>
  <div class="hidden-content">
    <p>3RD SHOW MORE AS A TEST</p>
  </div>
  <div class="button-wrapper" style="display: none;">
    <button class="show-more-btn">MORE!!</button>
  </div>
</div>


<script>
const buttons = document.querySelectorAll('.show-more-btn');

buttons.forEach((button, index) => {
  button.addEventListener('click', () => {
    const section = button.closest('.content-section');
    const hidden = section.querySelector('.hidden-content');
    const wrapper = button.closest('.button-wrapper');

    hidden.style.display = 'block';
    wrapper.style.display = 'none';

    const nextWrapper = document.querySelectorAll('.button-wrapper')[index + 1];
    if (nextWrapper) {
      nextWrapper.style.display = 'block';
    }
  });
});

</script>

</body>
</html>
