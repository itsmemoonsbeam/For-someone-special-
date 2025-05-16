<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Letter to Someone Special</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      background: url('dreamy-background.jpg') center/cover no-repeat;
      color: #fff;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      overflow: hidden;
    }
    .container {
      width: 90%; max-width: 600px;
      margin: 60px auto;
      background: rgba(0, 0, 0, 0.6);
      padding: 20px;
      border-radius: 10px;
      backdrop-filter: blur(5px);
      position: relative;
    }
    .slide { display: none; opacity: 0; transition: opacity 1s ease; }
    .slide.active { display: block; opacity: 1; }
    .text { font-size: 1rem; line-height: 1.6; margin-bottom: 20px; }
    .nav { text-align: center; margin-top: 10px; }
    .nav button {
      background: #444;
      color: #fff;
      padding: 10px 20px;
      border: none;
      margin: 0 5px;
      border-radius: 5px;
      cursor: pointer;
    }
    img.scribble { width: 100%; border-radius: 5px; margin-bottom: 20px; }
    audio.bg { position: fixed; bottom: 10px; left: 10px; }
  </style>
</head>
<body>
  <audio class="bg" controls loop>
    <source src="tum_se_hi.mp3" type="audio/mp3">
    <source src="tu_jaane_na.mp3" type="audio/mp3">
    <source src="blue.mp3" type="audio/mp3">
  </audio>
  <div class="container">
    <!-- Slide 1: Handwritten letter -->
    <div class="slide active" id="slide1">
      <div class="text">
        Dear Sakshi, my Dukhi Aatma…<br><br>
        I don’t know how to say this perfectly, but I need to speak from where it hurts… and where it still quietly hopes. 💭💫<br><br>
        Maybe we both stopped trying… What I care about—is *you*.<br><br>
        <em>Click "Next" to see more…</em>
      </div>
    </div><!-- Slide 2: Scribble image -->
<div class="slide" id="slide2">
  <img src="scribble1.jpg" alt="Memory" class="scribble">
  <div class="text"><em>Our old moments, scribbled in time.</em></div>
</div>

<!-- Slide 3: Text continuation -->
<div class="slide" id="slide3">
  <div class="text">
    Even when I seem rude… I still care. I’m still that same idiot… you called me Batman. 🦇💫<br><br>
    Click "Next"…
  </div>
</div>

<!-- Slide 4: More scribble -->
<div class="slide" id="slide4">
  <img src="scribble2.jpg" alt="Gossip memories" class="scribble">
  <div class="text"><em>Every detail you shared… I still wait for that.</em></div>
</div>

<!-- Slide 5: Voice TTS message -->
<div class="slide" id="slide5">
  <div class="text">
    <button id="playTTS">Hear My Heart</button>
  </div>
</div>

<!-- Navigation -->
<div class="nav">
  <button onclick="prevSlide()">Previous</button>
  <button onclick="nextSlide()">Next</button>
</div>

  </div>  <script>
    const slides = document.querySelectorAll('.slide');
    let current = 0;
    function showSlide(idx) {
      slides[current].classList.remove('active');
      current = (idx + slides.length) % slides.length;
      slides[current].classList.add('active');
    }
    function nextSlide() { showSlide(current + 1); }
    function prevSlide() { showSlide(current - 1); }

    // TTS setup
    document.getElementById('playTTS').addEventListener('click', () => {
      const msg = new SpeechSynthesisUtterance(
        "I want you back so badly, please come back, please 🥺"
      );
      msg.rate = 0.9;
      msg.pitch = 1.1;
      speechSynthesis.speak(msg);
    });
  </script></body>
</html>
