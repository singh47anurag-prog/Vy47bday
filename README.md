<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Dearest Vaishnavi ❤️</title>

    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.11.4/gsap.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

    <style>
        :root {
            --bg-color: #2a0a2a;
            --primary-color: #ff3879;
            --secondary-color: #ff74a4;
            --accent-glow: rgba(255, 100, 150, 0.6);
            --card-bg: rgba(255, 150, 200, 0.1);
            --card-border: rgba(255, 200, 220, 0.25);
            --text-light: #fce7f3;
        }

        body {
            margin: 0;
            font-family: sans-serif;
            background-color: var(--bg-color);
            color: var(--text-light);
            overflow: hidden;
        }

        #aurora-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(at 15% 15%, hsla(330, 80%, 75%, .5) 0px, transparent 60%),
                        radial-gradient(at 85% 20%, hsla(300, 70%, 70%, .4) 0px, transparent 60%);
            animation: aurora-flow 30s infinite alternate;
            background-size: 200% 200%;
            z-index: 0;
        }

        @keyframes aurora-flow {
            0% { background-position: 0% 50%; }
            100% { background-position: 100% 50%; }
        }

        .step {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(.95);
            opacity: 0;
            background: var(--card-bg);
            backdrop-filter: blur(20px);
            border: 1px solid var(--card-border);
            padding: 40px;
            border-radius: 30px;
            width: 90%;
            max-width: 750px;
            text-align: center;
            transition: all .7s ease;
            z-index: 2;
        }

        .step.active {
            opacity: 1;
            transform: translate(-50%, -50%) scale(1);
        }

        .btn {
            margin-top: 20px;
            padding: 12px 30px;
            border-radius: 999px;
            border: none;
            font-weight: bold;
            background: linear-gradient(90deg, var(--secondary-color), var(--primary-color));
            color: white;
            cursor: pointer;
            box-shadow: 0 0 30px var(--accent-glow);
            transition: .4s;
        }

        .btn:hover {
            transform: translateY(-6px) scale(1.05);
            box-shadow: 0 0 60px var(--accent-glow);
        }

        .text-gradient {
            background: linear-gradient(90deg, #ffc2e2, #ff8ab6, #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
    </style>
</head>

<body>

<!-- 🎵 MUSIC (Replace your-music.mp3 with your file name) -->
<audio autoplay loop>
    <source src="your-music.mp3" type="audio/mpeg">
</audio>

<div id="aurora-background"></div>

<div id="step1" class="step active">
    <h1 class="text-gradient text-4xl">Hello, My Vaishnavi ❤️</h1>
    <p>Every beat of my heart whispers your name, Vaishnavi.</p>
    <button class="btn" onclick="nextStep()">Unwrap My Feelings</button>
</div>

<div id="step2" class="step">
    <h1 class="text-gradient text-4xl">To My Beautiful Vaishnavi, Happy Birthday!</h1>
    <p>You illuminate my world more than the stars ever could.</p>
    <button class="btn" onclick="nextStep()">Discover More...</button>
</div>

<div id="step3" class="step">
    <h2 class="text-gradient text-3xl">Reasons I Adore You</h2>
    <p>
        💖 Your magical laughter<br><br>
        🧠 Your brilliant mind<br><br>
        🌸 Your pure and gentle soul
    </p>
    <button class="btn" onclick="nextStep()">One Final Thought...</button>
</div>

<div id="step4" class="step">
    <h2 class="text-gradient text-3xl">My Deepest Wish For You</h2>
    <p>May your life be filled with boundless joy and endless love.</p>
    <h1 class="text-gradient text-4xl" style="margin-top:25px;">
        Happy Birthday, My Dearest Vaishnavi! ❤️
    </h1>
    <button class="btn" onclick="celebrate()">Let's Celebrate!</button>
</div>

<script>
let currentStep = 1;
const totalSteps = 4;

function nextStep() {
    document.getElementById("step" + currentStep).classList.remove("active");
    currentStep++;
    document.getElementById("step" + currentStep).classList.add("active");
}

function celebrate() {
    confetti({
        particleCount: 300,
        spread: 160,
        origin: { y: 0.6 }
    });
}
</script>

</body>
</html>
