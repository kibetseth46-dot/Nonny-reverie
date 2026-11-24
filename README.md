
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Quiet Kind of Wonder | For Nonny</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    min-height: 100vh;
    font-family: Georgia, serif;
    color: #fff0f3;
    background:
      radial-gradient(circle at top, #783047, transparent 55%),
      linear-gradient(145deg, #190610, #490d25, #210714);
    overflow-x: hidden;
    text-align: center;
}

.stars {
    position: fixed;
    inset: 0;
    pointer-events: none;
    background-image:
      radial-gradient(2px 2px at 20% 30%, #fff 50%, transparent),
      radial-gradient(2px 2px at 70% 20%, #f7c5d0 50%, transparent),
      radial-gradient(2px 2px at 85% 75%, #fff 50%, transparent),
      radial-gradient(2px 2px at 35% 85%, #e7b5c3 50%, transparent);
    background-size: 180px 180px;
    animation: sparkle 5s infinite alternate;
}

@keyframes sparkle {
    from { opacity: .35; }
    to { opacity: 1; }
}

.container {
    position: relative;
    z-index: 2;
    width: 90%;
    max-width: 650px;
    margin: 55px auto;
    padding: 35px 24px;
    border: 1px solid rgba(226, 178, 151, .5);
    border-radius: 25px;
    background: rgba(40, 7, 23, .72);
    box-shadow: 0 0 35px rgba(220, 135, 160, .2);
    animation: appear 2s ease;
}

@keyframes appear {
    from {
        opacity: 0;
        transform: translateY(25px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.small-title {
    color: #e7b58e;
    letter-spacing: 5px;
    font-size: 11px;
    text-transform: uppercase;
}

h1 {
    font-size: clamp(30px, 8vw, 43px);
    color: #f5c6d0;
    font-weight: normal;
    margin: 20px 0 8px;
    text-shadow: 0 0 20px rgba(255, 190, 210, .5);
}

.subtitle {
    color: #e8b68e;
    font-size: 17px;
    font-style: italic;
    margin-bottom: 35px;
}

.divider {
    color: #d9a477;
    letter-spacing: 8px;
    margin: 25px 0;
}

.poem {
    font-size: clamp(17px, 4.5vw, 20px);
    line-height: 2;
    color: #fff0f2;
    font-style: italic;
}

.stanza {
    margin-bottom: 27px;
    animation: glow 4s infinite alternate;
}

@keyframes glow {
    from { text-shadow: 0 0 2px #f8dce4; }
    to { text-shadow: 0 0 12px #e5a5bb; }
}

.closing {
    margin-top: 35px;
    color: #e9b58e;
    font-size: 16px;
    font-style: italic;
    line-height: 1.8;
}

button {
    margin-top: 28px;
    padding: 14px 25px;
    border: 1px solid #e6b38d;
    border-radius: 30px;
    color: #fff0f3;
    background: linear-gradient(120deg, #7b2544, #a34c67);
    font-family: Georgia, serif;
    font-size: 15px;
    cursor: pointer;
    box-shadow: 0 0 15px rgba(229, 165, 187, .25);
}

button:active {
    transform: scale(.96);
}

#secret {
    display: none;
    margin-top: 25px;
    color: #f2c49e;
    font-style: italic;
    line-height: 1.9;
    animation: appear 1.5s ease;
}

.petal {
    position: fixed;
    top: -30px;
    z-index: 1;
    color: #e9a6bb;
    pointer-events: none;
    animation: fall linear infinite;
}

@keyframes fall {
    to {
        transform: translateY(110vh) rotate(360deg);
    }
}

footer {
    margin-top: 30px;
    font-size: 12px;
    color: #c99a9f;
    letter-spacing: 2px;
}

</style>
</head>

<body>

<div class="stars"></div>

<div class="container">

    <div class="small-title">A little piece of my heart</div>

    <h1>A Quiet Kind of Wonder</h1>

    <div class="subtitle">For Nonny ♡</div>

    <div class="divider">✧ ♡ ✧</div>

    <div class="poem">

        <div class="stanza">
            Nonny walks in quiet light<br>
            A soft eclipse along the street<br>
            The kind that turns a passer's eyes<br>
            As though down brushed passed their feet.
        </div>

        <div class="stanza">
            Her grace is a whispered rumour<br>
            A bloom unfolding out of time<br>
            I watch pretending not to watch<br>
            Holding wonder like a rhyme.
        </div>

        <div class="stanza">
            If day must pass before we speak<br>
            Let this feeling simply stay<br>
            A seed tucked within my chest<br>
            Gathering courage day by day.
        </div>

    </div>

    <div class="divider">✧ ♡ ✧</div>

    <div class="closing">
        Some feelings are too beautiful to rush.
    </div>

    <button onclick="revealSecret()">
        Open a little secret ♡
    </button>

    <div id="secret">
        Perhaps you may never know how effortlessly<br>
        you became a beautiful thought in someone's world.<br><br>
        No promises. No pressure.<br>
        Just a quiet admiration that deserves to be expressed. ❤️
    </div>

    <footer>
        WRITTEN WITH ADMIRATION · 23 NOVEMBER
    </footer>

</div>

<script>
function revealSecret() {
    const secret = document.getElementById("secret");

    if (secret.style.display === "block") {
        secret.style.display = "none";
    } else {
        secret.style.display = "block";
    }
}

// Floating rose petals
for (let i = 0; i < 18; i++) {
    let petal = document.createElement("div");
    petal.className = "petal";
    petal.innerHTML = "❀";

    petal.style.left = Math.random() * 100 + "vw";
    petal.style.animationDuration =
        (7 + Math.random() * 9) + "s";

    petal.style.animationDelay =
        (Math.random() * 10) + "s";

    petal.style.fontSize =
        (12 + Math.random() * 15) + "px";

    document.body.appendChild(petal);
}
</script>

</body>
</html>
