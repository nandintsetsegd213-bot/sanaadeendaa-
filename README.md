# sanaadeendaa-<!DOCTYPE html>
<html lang="mn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Чамд 💗</title>

<style>
*{box-sizing:border-box}

body{
    margin:0;
    height:100vh;
    overflow:hidden;
    font-family:Arial,sans-serif;
    background:
    radial-gradient(circle at 20% 20%,#ffd6e7 0%,transparent 35%),
    radial-gradient(circle at 80% 80%,#dcd6ff 0%,transparent 35%),
    linear-gradient(135deg,#fff1f6,#eeeaff);
    display:flex;
    justify-content:center;
    align-items:center;
}

.star{
    position:fixed;
    color:white;
    animation:twinkle 2s infinite alternate;
}

@keyframes twinkle{
    from{opacity:.2;transform:scale(.7)}
    to{opacity:1;transform:scale(1.3)}
}

.card{
    width:90%;
    max-width:420px;
    padding:35px 25px;
    text-align:center;
    border-radius:35px;
    background:rgba(255,255,255,.82);
    backdrop-filter:blur(18px);
    box-shadow:0 20px 60px rgba(100,70,130,.22);
    position:relative;
    z-index:10;
}

.heart{
    font-size:65px;
    animation:heartbeat 1.3s infinite;
}

@keyframes heartbeat{
    0%,100%{transform:scale(1)}
    50%{transform:scale(1.18)}
}

h1{
    color:#b51f5b;
    font-size:27px;
    margin:15px 0 10px;
}

.question{
    color:#4f4f5f;
    font-size:16px;
    margin-bottom:25px;
}

button{
    border:2px solid transparent;
    border-radius:30px;
    padding:14px 28px;
    margin:8px;
    font-size:16px;
    font-weight:bold;
    cursor:pointer;
    transition:.3s;
}

.yes{
    background:#c92f6d;
    color:white;
    box-shadow:0 8px 20px rgba(180,35,95,.35);
}

.no{
    background:white;
    color:#a51f58;
    border-color:#a51f58;
}

button:hover{
    transform:scale(1.08);
}

#final{
    display:none;
}

.sky{
    position:relative;
    height:120px;
    overflow:hidden;
}

.plane{
    position:absolute;
    font-size:70px;
    left:-100px;
    top:20px;
    animation:fly 4s linear infinite;
}

@keyframes fly{
    0%{left:-100px;transform:rotate(-5deg)}
    50%{left:50%;transform:rotate(0deg)}
    100%{left:110%;transform:rotate(5deg)}
}

.cloud{
    position:absolute;
    font-size:40px;
    opacity:.6;
}

.cloud1{left:5%;top:5px}
.cloud2{right:5%;bottom:0}

.love{
    color:#a51f58;
    font-size:24px;
    font-weight:bold;
    line-height:1.6;
}

.small{
    color:#4f4f5f;
    font-size:16px;
    line-height:1.7;
}

.floating{
    position:fixed;
    bottom:-30px;
    animation:up 5s linear forwards;
    pointer-events:none;
    z-index:2;
}

@keyframes up{
    0%{
        transform:translateY(0) rotate(0);
        opacity:0;
    }
    20%{opacity:1}
    100%{
        transform:translateY(-110vh) rotate(360deg);
        opacity:0;
    }
}

#noMessage{
    display:none;
    color:#a51f58;
    font-size:14px;
    margin-top:10px;
}
</style>
</head>

<body>

<!-- ✨ Одод -->
<script>
for(let i=0;i<35;i++){
    let star=document.createElement("div");
    star.className="star";
    star.innerHTML="✦";
    star.style.left=Math.random()*100+"vw";
    star.style.top=Math.random()*100+"vh";
    star.style.fontSize=(5+Math.random()*12)+"px";
    star.style.animationDelay=Math.random()*2+"s";
    document.body.appendChild(star);
}
</script>

<!-- 💗 ЭХЛЭЛ -->
<div class="card" id="question">

    <div class="heart">💗</div>

    <h1>Намайг санаж байна уу?</h1>

    <div class="question">
        Үнэнээ л хэлээрэй... 🥺
    </div>

    <button class="yes" onclick="yes()">
        Тийм ээ ❤️
    </button>

    <button class="no" onclick="no()">
        Үгүй 😗
    </button>

    <div id="noMessage">
        Үгүй гэж хэлэх эрхгүй шүү 🥹💕
    </div>

</div>


<!-- ✈️ ТӨГСГӨЛ -->
<div class="card" id="final">

    <div class="sky">

        <div class="cloud cloud1">☁️</div>
        <div class="cloud cloud2">☁️</div>

        <div class="plane">
            ✈️
        </div>

    </div>

    <div class="heart">
        💗
    </div>

    <div class="love">
        Би таныг машшшшш их<br>
        санажжж байнааа 🥺❤️
    </div>

    <br>

    <div class="small">
        Одоо онгоцонд суугаад<br>
        оччих уу миний хайрааа? ✈️🥹
    </div>

    <div style="font-size:30px;margin-top:18px;">
        💕 🌷 ✨ 🥹 ✨ 🌷 💕
    </div>

</div>


<script>

function yes(){

    document.getElementById("question").style.display="none";

    document.getElementById("final").style.display="block";

    hearts();
}


function no(){

    document.getElementById("noMessage").style.display="block";

    let btn=document.querySelector(".no");

    btn.innerHTML="Дахиад бод доо 🥺";

    btn.style.transform=
        "translate("+
        (Math.random()*100-50)+"px,"+
        (Math.random()*60-30)+"px)";
}


function hearts(){

    let symbols=[
        "❤️",
        "💗",
        "💕",
        "💖",
        "✨",
        "🌷",
        "🥹",
        "⭐"
    ];

    for(let i=0;i<45;i++){

        let h=document.createElement("div");

        h.className="floating";

        h.innerHTML=
            symbols[
                Math.floor(
                    Math.random()*symbols.length
                )
            ];

        h.style.left=
            Math.random()*100+"vw";

        h.style.fontSize=
            (15+Math.random()*25)+"px";

        h.style.animationDuration=
            (3+Math.random()*4)+"s";

        h.style.animationDelay=
            Math.random()*2+"s";

        document.body.appendChild(h);
    }
}

</script>

</body>
</html>
