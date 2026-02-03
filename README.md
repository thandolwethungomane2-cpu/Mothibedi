<!DOCTYPE html>
<html>
<head>
  <title>My Valentine ❤️</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Light romantic font -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,500&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      background: black;
      overflow: hidden;
      font-family: 'Playfair Display', serif;
    }

    .slide {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-size: cover;
      background-position: center;
    }

    .slide.active {
      display: block;
    }

    .note {
      position: absolute;
      bottom: 12%;
      left: 50%;
      transform: translateX(-50%);
      color: #fff;
      background: rgba(0,0,0,0.4);
      padding: 20px 25px;
      border-radius: 15px;
      font-size: 20px;
      text-align: center;
      max-width: 85%;
      animation: fadeIn 2s;
    }

    .tap {
      position: absolute;
      top: 5%;
      width: 100%;
      text-align: center;
      color: rgba(255,255,255,0.7);
      font-size: 14px;
      letter-spacing: 1px;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translate(-50%, 20px); }
      to { opacity: 1; transform: translate(-50%, 0); }
    }
  </style>
</head>
<body onclick="nextSlide()">

  <!-- Slide 1 -->
  <div class="slide active" style="background-image: url('pic1.jpg')">
    <div class="tap">Tap anywhere ❤️</div>
    <div class="note">
      To the most stunning woman emhlabeni ✨
    </div>
  </div>

  <!-- Slide 2 -->
  <div class="slide" style="background-image: url('pic2.jpg')">
    <div class="tap">Tap anywhere ❤️</div>
    <div class="note">
      Song of Solomon 4:7 is just an opening to describe just the Proverbs woman you are 💖
    </div>
  </div>

  <!-- Slide 3 -->
  <div class="slide" style="background-image: url('pic3.jpg')">
    <div class="tap">Tap anywhere ❤️</div>
    <div class="note" style="font-size: 26px;">
      Will you be my Valentine? 💘
    </div>
  </div>

  <script>
    let current = 0;
    const slides = document.querySelectorAll('.slide');

    function nextSlide() {
      slides[current].classList.remove('active');
      current = (current + 1) % slides.length;
      slides[current].classList.add('active');
    }
  </script>

</body>
</html>
