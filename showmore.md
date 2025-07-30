
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
.hidden-content {
  display: none;
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
    <p>I loved Science and Math when I was a kid. It fascinated me! I am grateful for my mother that she let me buy all the story books related to scientists, inventors and mathematicians (I can still remember the scenes I imagined as a kid when I read them). My love for them obviously transformed into love for Physics, which got transformed to mechanics/mechanical engineering eventually finding my core niche as Heat and mass transfer and computer simulations now.</p>

<p>Personally, I have a lot of other diverse interests -</p>

<p><strong>I love music!</strong> What’s my genre? None and all. I do have special place for western classical, but otherwise, I like good music. A good music is like truth - noone can deny it. Also, I attended a Hans Zimmer concert in 2023. What!? It’s worth mentioning twice!</p>

<p>I’ve realised that it’s not something that I absolutely love, but <strong>I am good at table tennis</strong>.</p>

<p><strong>I have recently started loving films</strong> actually. Or now that I think, I have started appreciating the art in them, because again, I have started understanding art more in itself.</p>

<p>I don’t know if I like philosophy (atleast, anymore) but <strong>I am a philosophical man</strong>. I do ask a lot of questions, but asking them for 25 years and going mad, a chapter from a book made my realise that it’s important to ask the right questions. It’s another thing that I still ask wrong questions though (inserts Captain America: I can do this all day gif*)</p>

<p><strong>I love psychology!</strong> I can get pretty obsessed with it sometimes, a behavior which I am not a fan of.</p>

<p><strong>I have taken quite some liking to literature</strong>, especially flash fiction and short stories. I like to make lists of books I wanna read instead of actually reading them - it’s one my guilty pleasures. Also, I think I am too dumb for poems, but I absolutey love poetic things!</p>

<p><strong>I have started loving to create content.</strong> I first had the taste of it when I made MechStuff - a blog on mechanical engineering and a YouTube channel associated with it almost a decade ago. I have had some rough years recently and now I wanna create personal content - about me, my thoughts, my feelings and emotions, my humor, my insights and whatever other nouns I can’t think of right now. Although a bit slow, I am glad that it has begun. This website is a proof :)</p>

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
