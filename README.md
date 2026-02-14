
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Valentine Website</title>
<style>
  body {
    margin: 0;
    font-family: "Comic Sans MS", "Poppins", cursive;
    background: linear-gradient(#ffb6d9, #ffcce6);
    color: white;
    text-align: center;
  }
  h1, h2, p {
    color: white;
    text-shadow: 2px 2px 5px #ff69b4;
  }
  .btn {
    background: #ff69b4;
    color: white;
    padding: 12px 24px;
    margin: 10px;
    border: 3px solid black;
    border-radius: 20px;
    font-size: 22px;
    cursor: pointer;
    box-shadow: 0 0 10px #ff69b4;
    transition: 0.3s;
  }
  .btn:hover {
    transform: scale(1.1);
  }
  #noBtn {
    position: absolute;
  }
  .gif-container img {
    width: 180px;
    margin: 10px;
    border: 3px solid black;
    border-radius: 18px;
    box-shadow: 0 0 12px #ff85c2;
    transition: 0.3s;
  }
  .gif-container img:hover {
    transform: scale(1.1);
  }
  .img-display {
    width: 260px;
    border: 3px solid black;
    border-radius: 20px;
    box-shadow: 0 0 15px #ff69b4;
  }
</style>
</head>
<body>

<!-- PAGE 1 -->
<div id="page1">
  <h1>Will you be my Valentine??? 💖</h1>
  <img src="pic1.jpg" class="img-display" />
  <br><br>
  <button class="btn" onclick="yesClicked()">Yes 😍</button>
  <button class="btn" id="noBtn" onclick="moveNo()">No 😭</button>
</div>

<!-- PAGE 2 -->
<div id="page2" style="display:none;">
  <h1>Here are your gifts Cutiee 🎁💘</h1>
  <img src="pic2.jpg" class="img-display" />
  <div class="gif-container">
    <img src="gif.gif" onclick="goTo(3)">
    <img src="gif.gif" onclick="goTo(4)">
    <img src="gif.gif" onclick="goTo(5)">
    <img src="gif.gif" onclick="goTo(6)">
  </div>
</div>

<!-- PAGE 3 (Kiss) -->
<div id="page3" style="display:none;">
  <h1>Here is your valentine kiss cutiee 😘💋</h1>
  <img src="pic3.jpg" class="img-display" />
  <br><button class="btn" onclick="backToGifts()">Back 🔙</button>
</div>

<!-- PAGE 4 (Rose) -->
<div id="page4" style="display:none;">
  <h1>Here is your rose Cutiee 🌹💕</h1>
  <img src="pic4.jpg" class="img-display" />
  <br><button class="btn" onclick="backToGifts()">Back 🔙</button>
</div>

<!-- PAGE 5 (Chocolate) -->
<div id="page5" style="display:none;">
  <h1>Here is your chocolate Cutiee 🍫💗</h1>
  <img src="pic5.jpg" class="img-display" />
  <br><button class="btn" onclick="backToGifts()">Back 🔙</button>
</div>

<!-- PAGE 6 (Sorry Note) -->
<div id="page6" style="display:none;">
  <h1>I'm really sorry, Cutiee 😔💞</h1>
  <img src="pic6.jpg" class="img-display" />
  <p style="width:80%; margin:auto; font-size:20px;">
    I'm really sorry for not talking to you. I never meant to hurt you, and it
    truly matters to me that you're happy. Please forgive me, Cutiee — your smile
    means the world to me and I promise to do better always. 💖🙏
  </p>
</div>

<script>
function yesClicked() {
  document.getElementById("page1").style.display = "none";
  document.getElementById("page2").style.display = "block";
}

function moveNo() {
  const btn = document.getElementById("noBtn");
  const x = Math.random() * (window.innerWidth - 100);
  const y = Math.random() * (window.innerHeight - 50);
  btn.style.left = x + "px";
  btn.style.top = y + "px";
}

function goTo(page) {
  document.getElementById("page2").style.display = "none";
  document.getElementById("page" + page).style.display = "block";
}

function backToGifts() {
  for (let i = 3; i <= 6; i++) {
    document.getElementById("page" + i).style.display = "none";
  }
  document.getElementById("page2").style.display = "block";
}
</script>

</body>
</html>

