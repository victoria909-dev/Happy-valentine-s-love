<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Valentine Vestor ❤️</title>
<style>
/* Background & font */
body {
  background: linear-gradient(to bottom, #ffb6c1, #ffe4e1);
  font-family: 'Comic Sans MS', cursive;
  text-align: center;
  overflow-x: hidden;
  padding: 20px;
}

/* Main box styling */
.box {
  background: white;
  max-width: 700px;
  margin: auto;
  border-radius: 25px;
  padding: 25px;
  box-shadow: 0px 0px 20px pink;
  position: relative;
  z-index: 2;
}

/* Headings & text */
h1 {
  color: #b30000;
  font-size: 40px;
  animation: pulse 1.5s infinite;
}

@keyframes pulse {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.05); }
}

p {
  font-size: 20px;
  color: #4d0000;
  margin: 15px 0;
}

/* Heart animation */
.heart-float {
  position: absolute;
  font-size: 25px;
  animation: float 8s linear infinite;
}

@keyframes float {
  0% { transform: translateY(100vh) translateX(0) rotate(0deg); opacity:0;}
  25% { opacity:1; }
  50% { transform: translateY(50vh) translateX(50px) rotate(180deg); }
  75% { opacity:1; }
  100% { transform: translateY(-10vh) translateX(-50px) rotate(360deg); opacity:0;}
}

#hearts-container {
  position: fixed;
  top:0; left:0;
  width:100%;
  height:100%;
  pointer-events:none;
  z-index:1;
}

/* Memory photo styling */
.love-photo {
  max-width: 90%;
  border-radius: 20px;
  margin: 15px 0;
  box-shadow: 0 0 15px #ff9999;
  border: 5px solid #ff4d6d;
}

.photo-caption {
  font-size: 18px;
  color: #b30000;
  margin-bottom: 20px;
}

/* 10 Reasons list */
ul {
  text-align: left;
  display: inline-block;
  font-size: 18px;
  color: #990000;
  margin-top: 10px;
  opacity: 0;
}
ul li {
  margin: 8px 0;
  transform: translateX(-30px);
  opacity: 0;
}
</style>
</head>
<body>

<!-- Floating hearts container -->
<div id="hearts-container"></div>

<div class="box">
<h1>Hi babe 🥺❤️</h1>
<div class="heart">💖💘💞</div>

<p>I just want you to know that you make me really happy.</p>

<p>Thank you for supporting me in the ways you can, even when things are not easy.  
And I’m sorry if I’ve ever been ungrateful in any way 😔.</p>

<p>I’m really grateful to have you in my life, and I appreciate how you always make sure I’m comfortable  
(even though you make sure everyone is comfortable 😏, you’re the only special person to me).</p>

<p>I love your laughter, the way your body feels, every kiss, every touch, how your presence heals 
You're my peace,my fire, my safest place, my favorite home is your warm embrace, thank you for loving me so much
I may not show it or say it enough, but I really do love you so much.Thank you for loving me even on the days I’m hard to love, and for being patient with my moods and soft heart 😉.</p>

<p>I may not have money for gifts this year, but I do have feelings, prayers, wishes, love,  
and this little website made just for you 🥺💖</p>
<p id="typed-text"></p>

<h2>📸 Our Favorite Memory</h2>
<img src="IMG-20250905-WA0080.jpg" alt="Us Together" class="love-photo">
<div class="photo-caption">Our favorite memory 🥰</div>

<h2>💌 10 Reasons I Love You</h2>
<ul id="love-list">
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
// Floating hearts function
function createHeart() {
  const heart = document.createElement('div');
  heart.className = 'heart-float';
  heart.style.left = Math.random() * window.innerWidth + 'px';
  heart.style.fontSize = 20 + Math.random() * 20 + 'px';
  const colors = ['#ff4d6d','#ff99c8','#cc66ff'];
  heart.style.color = colors[Math.floor(Math.random() * colors.length)];
  heart.style.animationDuration = 4 + Math.random()*6 + 's';
  heart.innerText = '💖';
  document.getElementById('hearts-container').appendChild(heart);
  setTimeout(() => heart.remove(), 10000);
}
setInterval(createHeart, 400);

// Typing animation
const message = `Hi babe 🥺\nI just want you to know that you make me really happy.\nThank you for supporting me even when things are not easy.\nI’m grateful to have you in my life and you’re my special person 😏❤️.`;
let index = 0;
const typedText = document.getElementById('typed-text');
function type() {
  if(index < message.length){
    typedText.innerHTML += message.charAt(index) === '\n' ? '<br>' : message.charAt(index);
    index++;
    setTimeout(type, 50);
  }
}
type();

// 10 Reasons slide-in animation
const listItems = document.querySelectorAll('#love-list li');
listItems.forEach((li, i) => {
  setTimeout(() => {
    li.style.transition = 'all 0.6s ease';
    li.style.opacity = 1;
    li.style.transform = 'translateX(0)';
  }, i*400 + 2000); // start after typing animation
});
</script>

</body>
</html>
