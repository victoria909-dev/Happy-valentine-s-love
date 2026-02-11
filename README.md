<html>
<head>
<meta charset="UTF-8">
<title>Happy Valentine Vestor ❤️</title>

<style>
body {
  background: linear-gradient(to bottom, #ffb6c1, #ffe4e1);
  text-align: center;
  font-family: 'Comic Sans MS', cursive;
  padding: 20px;
  overflow-x: hidden;
  line-height: 1.8;
}

h1 {
  color: #b30000;
  font-size: 38px;
}

h2 {
  color: #b30000;
}

p {
  font-size: 20px;
  color: #4d0000;
  margin-bottom: 18px;
}

/* Main card */
.box {
  background: white;
  padding: 25px;
  border-radius: 25px;
  box-shadow: 0 0 15px pink;
  max-width: 720px;
  margin: auto;
  position: relative;
  z-index: 2;
}

/* Typing (SHORT lines only) */
.typing {
  border-right: 2px solid #b30000;
  display: inline-block;
  white-space: nowrap;
  overflow: hidden;
}

/* Fade-in paragraphs */
.fade {
  opacity: 0;
  transform: translateY(10px);
  animation: fadeIn 1.5s forwards;
}

@keyframes fadeIn {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Hearts */
#hearts-container {
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: 1;
}

.heart-float {
  position: absolute;
  font-size: 22px;
  animation: float 4s linear forwards;
  opacity: 0;
}

@keyframes float {
  0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
  20% { opacity: 1; }
  100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
}

/* Image */
.photo-frame {
  border: 6px dashed #ff99c8;
  border-radius: 25px;
  padding: 10px;
  background: #fff0f5;
  display: inline-block;
}

.love-photo {
  max-width: 90%;
  border-radius: 15px;
  box-shadow: 0 0 10px #ff9999;
}

.caption {
  font-size: 16px;
  color: #990000;
  margin-top: 6px;
}

/* Reasons */
ul {
  list-style: none;
  padding: 0;
  display: inline-block;
  text-align: left;
}

ul li {
  opacity: 0;
  transform: translateX(-30px);
  animation: slideIn 0.8s forwards;
  margin-bottom: 8px;
  color: #990000;
  font-size: 18px;
}

@keyframes slideIn {
  to {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>
</head>

<body>

<audio autoplay loop>
  <source src="valentine-music.mp3" type="audio/mpeg">
</audio>

<div id="hearts-container"></div>

<div class="box">
<h1>Hi babe 🥺❤️</h1>

<p class="fade">I just want you to know that you make me really happy.</p>

<p class="fade">Thank you for supporting me in the ways you can, even when things are not easy and I’m sorry if I’ve ever been ungrateful in any way 😔.</p>

<p class="fade">I’m really grateful to have you in my life, and I appreciate how you always make sure I’m comfortable (even though you make sure everyone is comfortable 😏, you’re the only special person to me).</p>

<p class="fade">I love your laughter, the way your body feels, every kiss, every touch, how your presence heals. you're my peace, my fire, my safest place, my favorite home is your warm embrace.</p>

<p class="fade">Thank you for loving me so much. I may not show it or say it enough, but I really do love you so much.thank you for loving me even on the days I’m hard to love, and for being patient with my moods and soft heart 😉.</p>

<p class="fade">I may not have money for gifts this year, but I do have feelings, prayers, wishes, love and this little website made just for you 🥺💖</p>

<h2>📸 A Special Memory of us</h2>
<div class="photo-frame">
  <img src="https://i.imgur.com/7Y5O2YX.jpg" class="love-photo">
  <div class="caption">A moment I’ll cherish forever 💕</div>
</div>

<h2>💌 10 Reasons I Love You</h2>
<ul id="reasons">
<li>You make me laugh even when I’m upset 😄</li>
<li>You support me in ways big and small 🙏</li>
<li>You notice the little things about me 💕</li>
<li>You’re kind, patient, and understanding 🥰</li>
<li>You make me feel safe and comfortable 😌</li>
<li>You believe in me even when I doubt myself 💪</li>
<li>You’re my favorite person to talk to 📞</li>
<li>You have a heart that loves unconditionally ❤️</li>
<li>You make everyday brighter 🌞</li>
<li>Simply because YOU are YOU, and that’s perfect for me 😭💖</li>
</ul>

<p><b>Happy Valentine’s Day, my favorite person 💕</b></p>
<p>From: Your girlfriend (trying very hard not to be shy calling you babe 😭😂)</p>
</div>

<script>
// Floating hearts
function createHeart() {
  const heart = document.createElement('div');
  heart.className = 'heart-float';
  heart.innerText = '💖';
  heart.style.left = Math.random() * window.innerWidth + 'px';
  heart.style.fontSize = 18 + Math.random() * 22 + 'px';
  const colors = ['#ff4d6d','#ff99c8','#cc66ff'];
  heart.style.color = colors[Math.floor(Math.random() * colors.length)];
  document.getElementById('hearts-container').appendChild(heart);
  setTimeout(() => heart.remove(), 4000);
}
setInterval(createHeart, 300);

// Typing effect (safe)
const typing = document.querySelector('.typing');
const text = typing.innerText;
typing.innerText = '';
let i = 0;
const typeInterval = setInterval(() => {
  typing.innerText += text[i];
  i++;
  if (i === text.length) clearInterval(typeInterval);
}, 70);

// Slide-in reasons
document.querySelectorAll('#reasons li').forEach((li, i) => {
  li.style.animationDelay = `${i * 0.4}s`;
});
</script>

</body>
</html>
