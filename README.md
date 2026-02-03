<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Sunayna, Be My Valentine ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg, #ff4e8a, #ff9a9e);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Segoe UI', sans-serif;
    overflow: hidden;
    color: white;
}

.card {
    background: rgba(255, 255, 255, 0.18);
    padding: 35px;
    border-radius: 28px;
    text-align: center;
    backdrop-filter: blur(12px);
    box-shadow: 0 18px 45px rgba(0,0,0,0.35);
    max-width: 420px;
    animation: fadeIn 1.5s ease;
}

h1 {
    font-size: 2.3em;
    margin-bottom: 8px;
}

h2 {
    font-weight: 400;
    margin-bottom: 25px;
}

.buttons {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
}

button {
    border: none;
    padding: 14px 32px;
    font-size: 1.1em;
    border-radius: 30px;
    cursor: pointer;
    transition: transform 0.2s, box-shadow 0.2s;
}

.yes {
    background: #fff;
    color: #ff4e8a;
}

.no {
    background: rgba(255,255,255,0.4);
    color: white;
}

button:hover {
    transform: scale(1.1);
    box-shadow: 0 10px 25px rgba(0,0,0,0.35);
}

.message {
    display: none;
    margin-top: 22px;
    font-size: 1.2em;
    animation: fadeIn 1s ease;
}

.signature {
    margin-top: 18px;
    font-size: 0.95em;
    opacity: 0.9;
}

.heart {
    position: absolute;
    bottom: -50px;
    font-size: 22px;
    animation: floatUp 6s linear infinite;
    opacity: 0.75;
}

@keyframes floatUp {
    from { transform: translateY(0); }
    to { transform: translateY(-110vh); }
}

@keyframes fadeIn {
    from { opacity: 0; transform: scale(0.9); }
    to { opacity: 1; transform: scale(1); }
}
</style>
</head>

<body>

<div class="card">
    <h1>Sunayna Paladh ❤️</h1>
    <h2>Will you be my Valentine?</h2>

    <div class="buttons">
        <button class="yes" onclick="sayYes()">YES 💍</button>
        <button class="no" onmouseover="moveNo(this)">NO 😄</button>
    </div>

    <div class="message" id="loveMessage">
        💖 You just made my heart the happiest 💖  
        <br><br>
        I can’t wait to spend forever with you 🌹✨
    </div>

    <div class="signature">
        Forever yours,<br>
        <strong>Shivkar 💍</strong>
    </div>
</div>

<audio id="music" loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

<script>
function sayYes() {
    document.getElementById("loveMessage").style.display = "block";
    document.getElementById("music").play();
}

function moveNo(btn) {
    btn.style.position = "absolute";
    btn.style.left = Math.random() * 80 + "vw";
    btn.style.top = Math.random() * 80 + "vh";
}

// Floating hearts
for (let i = 0; i < 35; i++) {
    let heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (4 + Math.random() * 4) + "s";
    document.body.appendChild(heart);
}
</script>

</body>
</html>
