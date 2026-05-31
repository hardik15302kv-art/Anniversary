<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Love Letter ❤️</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Georgia, serif;
}

body{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:#ff9eb5;
overflow:hidden;
}

/* Hearts */
.hearts{
position:absolute;
width:100%;
height:100%;
overflow:hidden;
}

.hearts span{
position:absolute;
color:#e60026;
font-size:24px;
animation:float 8s linear infinite;
}

@keyframes float{
0%{
transform:translateY(100vh);
opacity:0;
}
20%{opacity:1;}
100%{
transform:translateY(-120px);
opacity:0;
}
}

/* Envelope */
.wrapper{
position:relative;
cursor:pointer;
}

.envelope{
position:relative;
width:280px;
height:190px;
background:#efd88a;
border-radius:0 0 6px 6px;
}

.envelope:before{
content:"";
position:absolute;
top:0;
left:0;
border-left:140px solid transparent;
border-right:140px solid transparent;
border-top:95px solid #e3c96f;
transform-origin:top;
transition:0.6s;
z-index:5;
}

.wrapper.open .envelope:before{
transform:rotateX(180deg);
}

/* Letter */
.letter{
position:absolute;
left:20px;
bottom:10px;
width:240px;
height:160px;
background:#fff;
border-radius:8px;
padding:15px;
text-align:center;
transition:0.7s;
z-index:2;
box-shadow:0 5px 15px rgba(0,0,0,0.15);
}

.wrapper.open .letter{
transform:translateY(-140px);
}

.letter h3{
font-size:24px;
margin-bottom:10px;
}

.letter p{
font-size:20px;
color:#444;
line-height:1.3;
}

.emoji{
font-size:50px;
margin-top:8px;
}
</style>
</head>

<body>

<div class="hearts"></div>

<div class="wrapper" onclick="toggleLetter()">
<div class="letter">
<p>
You are one in a million<br>
feeling, I love you! ❤️
</p>

<div class="emoji">🐰🧸</div>
</div>

<div class="envelope"></div>
</div>

<script>
function toggleLetter(){
document.querySelector('.wrapper').classList.toggle('open');
}

const hearts=document.querySelector('.hearts');

for(let i=0;i<30;i++){
let h=document.createElement('span');
h.innerHTML='❤';
h.style.left=Math.random()*100+'vw';
h.style.animationDuration=(5+Math.random()*5)+'s';
h.style.animationDelay=Math.random()*5+'s';
h.style.fontSize=(15+Math.random()*25)+'px';
hearts.appendChild(h);
}
</script>

</body>
</html># Anniversary
