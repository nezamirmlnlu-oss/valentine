<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Valentine 💕</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
* {
margin: 0;
padding: 0;
box-sizing: border-box;
}

body {
margin: 0;
height: 100vh;
background: linear-gradient(135deg, #ff9a9e, #fad0c4);
display: flex;
justify-content: center;
align-items: center;
font-family: 'Arial', sans-serif;
overflow: hidden;
position: relative;
}

.page {
display: none;
width: 100%;
height: 100vh;
justify-content: center;
align-items: center;
flex-direction: column;
animation: fadeIn 0.8s ease-in;
}

.page.active {
display: flex;
}

@keyframes fadeIn {
from { opacity: 0; transform: scale(0.9); }
to { opacity: 1; transform: scale(1); }
}

.card {
background: white;
padding: 40px;
border-radius: 20px;
text-align: center;
box-shadow: 0 10px 30px rgba(0,0,0,0.2);
width: 90%;
max-width: 400px;
position: relative;
animation: cardBounce 0.6s ease-out;
}

@keyframes cardBounce {
0% { transform: translateY(-100px); opacity: 0; }
60% { transform: translateY(10px); }
100% { transform: translateY(0); opacity: 1; }
}

h1 {
color: #ff4d6d;
margin-bottom: 25px;
font-size: 28px;
}

h2 {
color: #ff4d6d;
margin-bottom: 20px;
font-size: 24px;
}

p {
color: #555;
line-height: 1.8;
margin-bottom: 20px;
font-size: 16px;
}

button {
padding: 12px 30px;
font-size: 16px;
border: none;
border-radius: 25px;
cursor: pointer;
transition: transform 0.2s, box-shadow 0.2s;
margin: 10px;
}

button:hover {
transform: scale(1.05);
box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}

.yes {
background: #ff4d6d;
color: white;
}

.no {
background: #ddd;
position: absolute;
left: 20px;
top: 140px;
}

.continue-btn {
background: #ff6b9d;
color: white;
margin-top: 20px;
}

/* Floating hearts animation */
.heart {
position: absolute;
font-size: 30px;
animation: float 4s infinite;
opacity: 0.7;
}

@keyframes float {
0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
50% { opacity: 0.7; }
100% { transform: translateY(-100px) rotate(360deg); opacity: 0; }
}

/* Cuddle animation */
.cuddle-container {
display: flex;
justify-content: center;
align-items: center;
margin: 30px 0;
position: relative;
}

.cuddle-emoji {
font-size: 80px;
animation: cuddle 2s infinite ease-in-out;
margin: 0 -20px;
}

.cuddle-emoji:nth-child(2) {
animation-delay: 0.5s;
}

@keyframes cuddle {
0%, 100% { transform: translateX(0) rotate(0deg); }
25% { transform: translateX(-10px) rotate(-5deg); }
75% { transform: translateX(10px) rotate(5deg); }
}

/* Love letter styling */
.letter {
background: #fff9f0;
border: 2px solid #ff4d6d;
border-radius: 15px;
padding: 30px;
margin: 20px auto;
max-width: 450px;
box-shadow: 0 5px 20px rgba(0,0,0,0.15);
text-align: left;
}

.letter-header {
text-align: center;
color: #ff4d6d;
margin-bottom: 20px;
font-style: italic;
}

.signature {
text-align: right;
margin-top: 20px;
font-style: italic;
color: #ff4d6d;
}

/* Dancing hearts */
.hearts-dance {
position: absolute;
width: 100%;
height: 100%;
pointer-events: none;
}

/* Final celebration */
.celebration {
text-align: center;
color: white;
padding: 20px;
}

.celebration h1 {
color: white;
font-size: 48px;
margin-bottom: 30px;
animation: pulse 1.5s infinite;
}

@keyframes pulse {
0%, 100% { transform: scale(1); }
50% { transform: scale(1.1); }
}

.celebration-img {
width: 280px;
margin-top: 20px;
border-radius: 20px;
box-shadow: 0 10px 30px rgba(0,0,0,0.3);
animation: bounce 1s infinite;
}

@keyframes bounce {
0%, 100% { transform: translateY(0); }
50% { transform: translateY(-20px); }
}

/* Sparkles */
.sparkle {
position: absolute;
font-size: 20px;
animation: sparkle 1.5s infinite;
}

@keyframes sparkle {
0%, 100% { opacity: 0; transform: scale(0); }
50% { opacity: 1; transform: scale(1); }
}

.message-box {
background: rgba(255, 255, 255, 0.9);
padding: 25px;
border-radius: 15px;
max-width: 500px;
margin: 20px;
}
</style>
</head>
<body>

<!-- Floating hearts background -->
<div class="hearts-dance" id="heartsContainer"></div>

<!-- Page 1: Initial Question -->
<div class="page active" id="page1">
<div class="card">
<h1>💕 Hey yourname, will you be my Valentine? 💕</h1>
<button class="yes" onclick="goToPage(2)">Yes! 💖</button>
<button class="no" id="noBtn">No 😢</button>
</div>
</div>

<!-- Page 2: Love Letter 1 -->
<div class="page" id="page2">
<div class="letter">
<div class="letter-header">
<h2>💌 A Letter Just For You 💌</h2>
</div>
<p>Dear georgia,</p>
<p>From the moment I first saw you, I knew there was something special about you. Your smile lights up my world like sunshine breaking through clouds on a rainy day.</p>
<p>Every moment with you feels like a beautiful dream I never want to wake up from. You make ordinary days feel extraordinary, and you bring joy to my heart in ways I never knew were possible.</p>
<p>So today, I'm asking... will you let me be your Valentine? 💕</p>
<div class="signature">With all my love,<br>Your not meant to be husband  💖</div>
</div>
<button class="continue-btn" onclick="goToPage(3)">Continue 💕</button>
</div>

<!-- Page 3: Cuddle Animation -->
<div class="page" id="page3">
<div class="card">
<h2>This could be us... 🥰</h2>
<div class="cuddle-container">
<div class="cuddle-emoji">🧸</div>
<div class="cuddle-emoji">💕</div>
<div class="cuddle-emoji">🧸</div>
</div>
<p style="color: #ff4d6d; font-size: 18px;">...cuddling together! 💗</p>
<button class="continue-btn" onclick="goToPage(4)">Keep Reading 💌</button>
</div>
</div>

<!-- Page 4: Love Letter 2 -->
<div class="page" id="page4">
<div class="letter">
<div class="letter-header">
<h2>✨ More Reasons Why ✨</h2>
</div>
<p>Hey georgia,</p>
<p>I love the way you laugh - it's like music to my ears. I love how you make me feel comfortable being myself. I love your kindness, your warmth, and the way you care about the people around you.</p>
<p>Being with you feels like coming home. You're my happy place, my comfort, and my favorite person to talk to about anything and everything.</p>
<p>I promise to make you smile, to support you through everything, and to cherish every moment we spend together. 💕</p>
<div class="signature">Forever yours,<br>Someone who adores you 💖</div>
</div>
<button class="continue-btn" onclick="goToPage(5)">Next 🌟</button>
</div>

<!-- Page 5: More Cuddles -->
<div class="page" id="page5">
<div class="card">
<h2>Imagine all the hugs! 🤗</h2>
<div class="cuddle-container">
<div class="cuddle-emoji">👫</div>
<div class="cuddle-emoji">💗</div>
<div class="cuddle-emoji">💑</div>
</div>
<p style="color: #ff4d6d; font-size: 18px;">We could be the cutest couple! 💕✨</p>
<button class="continue-btn" onclick="goToPage(6)">Almost there! 💖</button>
</div>
</div>

<!-- Page 6: Love Letter 3 -->
<div class="page" id="page6">
<div class="letter">
<div class="letter-header">
<h2>💝 One Last Thing... 💝</h2>
</div>
<p>My Dearest georgia,</p>
<p>I know I might seem a little insecure (okay, maybe a lot insecure!), but that's only because you mean so much to me. You deserve someone who will appreciate you, make you laugh, and be there for you always.</p>
<p>I want to be that person for you. I want to create beautiful memories together, go on adventures, have movie nights, share inside jokes, and just enjoy every precious moment by your side.</p>
<p>So please, would you make this Valentine's Day (and every day after) special by being mine? 💕</p>
<div class="signature">With hope in my heart,<br>Your Valentine 💖</div>
</div>
<button class="continue-btn" onclick="goToPage(7)">Final Answer Time! 💕</button>
</div>

<!-- Page 7: Final Question -->
<div class="page" id="page7">
<div class="card">
<h1>So... what do you say, my georgia? 💕</h1>
<p style="font-size: 18px; color: #ff4d6d; margin: 20px 0;">Will you be my Valentine? 🥺💖</p>
<div class="cuddle-container">
<div class="cuddle-emoji">🌹</div>
<div class="cuddle-emoji">💕</div>
<div class="cuddle-emoji">🌹</div>
</div>
<button class="yes" onclick="yesClick()">YES! 💖</button>
<button class="no" id="noBtn2">No...</button>
</div>
</div>

<!-- Page 8: Celebration -->
<div class="page" id="page8">
<div class="celebration">
<h1>🎉 YAYYY baby! I KNEW IT! 🎉</h1>
<div class="message-box">
<h2>💕 You just made me the happiest person ever! 💕</h2>
<p style="color: #555; font-size: 18px;">Get ready for endless cuddles, sweet messages, cute dates, and all the love you deserve! 🥰</p>
<div class="cuddle-container">
<div class="cuddle-emoji">😍</div>
<div class="cuddle-emoji">💖</div>
<div class="cuddle-emoji">😍</div>
</div>
</div>
<img
src="https://media.giphy.com/media/3oriO0OEd9QIDdllqo/giphy.gif"
alt="Dancing celebration"
class="celebration-img"
>
<p style="font-size: 24px; margin-top: 30px;">You + Me = Perfect 💕✨</p>
</div>
</div>

<script>
// Create floating hearts
function createHeart() {
const heart = document.createElement('div');
heart.className = 'heart';
heart.innerHTML = '💕';
heart.style.left = Math.random() * 100 + '%';
heart.style.animationDuration = (Math.random() * 3 + 3) + 's';
heart.style.animationDelay = Math.random() * 2 + 's';
document.getElementById('heartsContainer').appendChild(heart);
setTimeout(() => heart.remove(), 7000);
}

// Generate hearts continuously
setInterval(createHeart, 500);

// Create sparkles
function createSparkle(x, y) {
const sparkle = document.createElement('div');
sparkle.className = 'sparkle';
sparkle.innerHTML = '✨';
sparkle.style.left = x + 'px';
sparkle.style.top = y + 'px';
document.body.appendChild(sparkle);
setTimeout(() => sparkle.remove(), 1500);
}

// Random sparkles
setInterval(() => {
createSparkle(Math.random() * window.innerWidth, Math.random() * window.innerHeight);
}, 1000);

// Page navigation
function goToPage(pageNum) {
document.querySelectorAll('.page').forEach(page => page.classList.remove('active'));
document.getElementById('page' + pageNum).classList.add('active');
}

// Moving No button for page 1
const noBtn = document.getElementById("noBtn");
if (noBtn) {
const card = noBtn.closest(".card");
function randomMove() {
const maxX = card.clientWidth - noBtn.offsetWidth - 40;
const maxY = card.clientHeight - noBtn.offsetHeight - 40;
const x = Math.random() * maxX + 20;
const y = Math.random() * maxY + 20;
noBtn.style.left = x + "px";
noBtn.style.top = y + "px";
}
setInterval(randomMove, 700);
}

// Moving No button for page 7
const noBtn2 = document.getElementById("noBtn2");
if (noBtn2) {
const card2 = noBtn2.closest(".card");
function randomMove2() {
const maxX = card2.clientWidth - noBtn2.offsetWidth - 40;
const maxY = card2.clientHeight - noBtn2.offsetHeight - 40;
const x = Math.random() * maxX + 20;
const y = Math.random() * maxY + 20;
noBtn2.style.left = x + "px";
noBtn2.style.top = y + "px";
}
setInterval(randomMove2, 700);
}

// Yes button click
function yesClick() {
goToPage(8);
// Create celebration sparkles
for (let i = 0; i < 20; i++) {
setTimeout(() => {
createSparkle(Math.random() * window.innerWidth, Math.random() * window.innerHeight);
}, i * 100);
}
}
</script>
</body>
</html>
