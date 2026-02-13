# Index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For You 💗</title>

<style>
body {
  margin: 0;
  font-family: 'Segoe UI', sans-serif;
  text-align: center;
  background: linear-gradient(135deg, #ffd6e7, #ffffff);
  overflow-x: hidden;
}

/* Card */
.container {
  margin: 50px auto;
  width: 90%;
  max-width: 520px;
  background: rgba(255,255,255,0.75);
  padding: 30px;
  border-radius: 20px;
  box-shadow: 0 10px 25px rgba(0,0,0,0.1);
  backdrop-filter: blur(10px);
}

h1 { color: #d6336c; }

/* Countdown */
.countdown {
  font-size: 20px;
  color: #ff4d88;
  font-weight: bold;
  margin-bottom: 15px;
}

/* Typewriter */
.typewriter {
  font-size: 18px;
  border-right: 3px solid pink;
  white-space: nowrap;
  overflow: hidden;
  margin: 20px auto;
  width: fit-content;
  animation: typing 4s steps(40), blink .7s infinite;
}

@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}
@keyframes blink {
  50% { border-color: transparent }
}

/* Highlight message */
.highlight {
  background: #ffe6f0;
  padding: 15px;
  border-radius: 15px;
  margin-top: 20px;
  font-style: italic;
  color: #d6336c;
  font-size: 17px;
}

/* Floating hearts */
.heart {
  position: fixed;
  font-size: 20px;
  pointer-events: none;
  animation: floatUp 2s linear forwards;
}
@keyframes floatUp {
  0% { transform: translateY(0); opacity: 1; }
  100% { transform: translateY(-150px); opacity: 0; }
}

/* Button */
button {
  margin-top: 20px;
  padding: 12px 25px;
  border: none;
  background: #ff4d88;
  color: white;
  border-radius: 25px;
  font-size: 16px;
  cursor: pointer;
}
</style>
</head>

<body>

<!-- Music -->
<audio autoplay loop>
<source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3">
</audio>

<div class="container">

<h1>For You 💗</h1>

<div class="countdown" id="days"></div>

<div class="typewriter">
You are always in my duas and my heart 🙂
</div>

<p>
I may not always know how to express feelings,<br>
but talking to you feels calm and comforting 🌸
</p>

<p>
Every day I notice small things about you…<br>
and somehow you feel more special than before ☺️
</p>

<p>
May Allah keep you happy,<br>
protect your heart,<br>
and guide you always 🤍
</p>

<!-- Highlight message -->
<div class="highlight">
"Yesterday I slept peacefully after so long…  
because you were the last thought in my mind."
</div>

<button onclick="showLove()">Click Me 💖</button>

</div>

<script>

/* COUNTDOWN DAYS SINCE JAN 6 */
const startDate = new Date("Jan 6, 2026");
const today = new Date();
const diffTime = today - startDate;
const days = Math.floor(diffTime / (1000*60*60*24));

document.getElementById("days").innerText =
"💞 " + days + " days of talking and counting...";

/* Popup message */
function showLove() {
  alert("Talking to you is my favorite part of the day 💗");
}

/* Heart swipe effect */
document.addEventListener("mousemove", createHeart);
document.addEventListener("touchmove", createHeart);

function createHeart(e) {
  let heart = document.createElement("div");
  heart.innerHTML = "💗";
  heart.className = "heart";
  heart.style.left = (e.pageX || e.touches[0].pageX) + "px";
  heart.style.top = (e.pageY || e.touches[0].pageY) + "px";
  document.body.appendChild(heart);
  setTimeout(() => heart.remove(), 2000);
}

</script>

</body>
</html>
