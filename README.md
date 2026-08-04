<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Diddy Sus | The Legends</title>

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
scroll-behavior:smooth;
}

body{

font-family:Poppins,sans-serif;
background:#050816;
color:white;
overflow-x:hidden;

}

/* Animated Background */

body::before{

content:"";
position:fixed;
top:0;
left:0;
width:100%;
height:100%;

background:
radial-gradient(circle at 20% 20%,rgba(0,255,255,.25),transparent 30%),
radial-gradient(circle at 80% 20%,rgba(140,0,255,.20),transparent 35%),
radial-gradient(circle at 50% 80%,rgba(0,120,255,.18),transparent 35%);

animation:bgMove 18s linear infinite;

z-index:-2;

}

@keyframes bgMove{

0%{
transform:translateY(0px);
}

50%{
transform:translateY(-30px);
}

100%{
transform:translateY(0px);
}

}

/* Floating Stars */

.stars{

position:fixed;

width:100%;
height:100%;

top:0;
left:0;

z-index:-1;

overflow:hidden;

}

.star{

position:absolute;

width:3px;
height:3px;

background:white;

border-radius:50%;

animation:float 12s linear infinite;

opacity:.8;

}

@keyframes float{

0%{

transform:translateY(100vh);

opacity:0;

}

10%{

opacity:1;

}

100%{

transform:translateY(-100vh);

opacity:0;

}

}

/* Hero */

header{

height:100vh;

display:flex;

justify-content:center;

align-items:center;

text-align:center;

flex-direction:column;

padding:20px;

}

header h1{

font-size:65px;

font-family:Orbitron,sans-serif;

text-shadow:
0 0 15px cyan,
0 0 40px blue;

margin-bottom:20px;

}

.typing{

font-size:24px;

color:#8fdcff;

min-height:40px;

}

/* Sections */

.section{

width:90%;

max-width:1100px;

margin:70px auto;

padding:35px;

background:rgba(255,255,255,.06);

backdrop-filter:blur(12px);

border:1px solid rgba(255,255,255,.15);

border-radius:20px;

box-shadow:

0 0 30px rgba(0,255,255,.08);

}

.section h2{

font-family:Orbitron,sans-serif;

font-size:34px;

margin-bottom:25px;

color:#72d9ff;

}

/* Cards */

.members{

display:grid;

grid-template-columns:repeat(auto-fit,minmax(220px,1fr));

gap:25px;

}

.card{

background:rgba(255,255,255,.08);

padding:18px;

border-radius:18px;

transition:.35s;

overflow:hidden;

border:1px solid rgba(255,255,255,.08);

}

.card:hover{

transform:translateY(-12px) scale(1.03);

box-shadow:

0 0 30px cyan,

0 0 50px blue;

}

.card img{

width:100%;

border-radius:15px;

margin-bottom:12px;

}

.card h3{

font-family:Orbitron,sans-serif;

margin-bottom:10px;

}

.quote{

text-align:center;

font-size:22px;

margin-top:30px;

color:#ffe66d;

}

footer{

padding:60px;

text-align:center;

color:#aaa;

font-size:15px;

}

</style>

</head>

<body>

<div class="stars" id="stars"></div>

<header>

<h1>DIDDY SUS</h1>

<div class="typing" id="typing"></div>

</header>
<div class="section">

<h2>Loading The Legends...</h2>

<p style="font-size:20px;line-height:1.8;text-align:center;">

Welcome to the official archive of the greatest friend group.

Every clutch.
Every joke.
Every late night.
Every memory.

This is where the legends live forever.

</p>

</div>

<script>

/* ===========================
   TYPING INTRO
=========================== */

const messages = [

"Loading Diddy Sus...",
"Finding the Legends...",
"Initializing Friend Group...",
"Friendship Status: LEGENDARY.",
"Welcome."

];

let message = 0;
let letter = 0;

const typing = document.getElementById("typing");

function type(){

if(letter < messages[message].length){

typing.innerHTML += messages[message].charAt(letter);

letter++;

setTimeout(type,70);

}

else{

setTimeout(()=>{

typing.innerHTML="";

letter=0;

message++;

if(message>=messages.length){

message=0;

}

type();

},1700);

}

}

type();

/* ===========================
   FLOATING STARS
=========================== */

const starContainer = document.getElementById("stars");

for(let i=0;i<150;i++){

const star=document.createElement("div");

star.className="star";

star.style.left=Math.random()*100+"%";

star.style.top=Math.random()*100+"%";

star.style.animationDuration=(6+Math.random()*10)+"s";

star.style.animationDelay=Math.random()*8+"s";

star.style.opacity=Math.random();

star.style.width=(2+Math.random()*4)+"px";

star.style.height=star.style.width;

starContainer.appendChild(star);

}

/* ===========================
   FADE IN ON SCROLL
=========================== */

const observer=new IntersectionObserver(entries=>{

entries.forEach(entry=>{

if(entry.isIntersecting){

entry.target.animate([

{

opacity:0,

transform:"translateY(60px)"

},

{

opacity:1,

transform:"translateY(0px)"

}

],{

duration:900,

fill:"forwards"

});

}

});

});

document.querySelectorAll(".section,.card").forEach(item=>{

observer.observe(item);

});

</script>
<div class="section">

<h2>🏆 Hall of Legends</h2>

<div class="members">

<div class="card" id="aidenCard">

<img src="YOUR_AIDEN_IMAGE_URL">

<h3>🎯 Aiden</h3>

<h4>Siege Master</h4>

<p>

Level: 99

Aim: ██████████

Game Sense: ██████████

Clutches: Infinite

</p>

</div>

<div class="card" id="gabeCard">

<img src="YOUR_GABE_IMAGE_URL">

<h3>🎮 Gabe</h3>

<h4>Professional Thrower</h4>

<p>

Aim: █

Luck: █

Funny Moments: ██████████

Finding New Ways To Lose: ██████████

</p>

</div>

<div class="card">

<img src="YOUR_ANTHONY_IMAGE_URL">

<h3>🔫 Anthony</h3>

<h4>FPS Machine</h4>

<p>

Shooter Skill: ██████████

Reaction Time: █████████

Kills: Too Many

</p>

</div>

<div class="card">

<img src="YOUR_JACKSON_IMAGE_URL">

<h3>👑 Sus</h3>

<h4>Built Different</h4>

<p>

Every Game Played:

Completed.

Every Lobby:

Fear.

</p>

</div>

<div class="card">

<img src="YOUR_JOSH_IMAGE_URL">

<h3>🧪 Josh</h3>

<h4>The Rick</h4>

<p>

Bravery: ██████████

Muscles: ██████████

Intelligence: █████████

Every Game Skill:

████████

</p>

</div>

</div>

</div>

<div class="section">

<h2>🎮 Press Start</h2>

<center>

<button id="startButton">

ENTER THE LEGENDS

</button>

</center>

</div>

<style>

#startButton{

margin-top:20px;

padding:20px 50px;

font-size:22px;

font-family:Orbitron;

background:#00bfff;

border:none;

border-radius:15px;

color:white;

cursor:pointer;

transition:.3s;

box-shadow:

0 0 20px cyan;

}

#startButton:hover{

transform:scale(1.08);

box-shadow:

0 0 35px cyan,

0 0 70px blue;

}

.cursor{

width:18px;

height:18px;

border-radius:50%;

position:fixed;

pointer-events:none;

background:cyan;

box-shadow:

0 0 20px cyan,

0 0 40px blue;

transform:translate(-50%,-50%);

z-index:99999;

}

</style>

<script>

/* RGB Cursor */

const cursor=document.createElement("div");

cursor.className="cursor";

document.body.appendChild(cursor);

document.addEventListener("mousemove",e=>{

cursor.style.left=e.clientX+"px";

cursor.style.top=e.clientY+"px";

});

/* Start Button */

document.getElementById("startButton").onclick=function(){

window.scrollTo({

top:document.querySelector(".section").offsetTop,

behavior:"smooth"

});

};

/* Gabe Easter Egg */

let gabeClicks=0;

document.getElementById("gabeCard").onclick=function(){

gabeClicks++;

if(gabeClicks==10){

alert("Achievement Unlocked!\n\nGabe finally won a game... maybe.");

gabeClicks=0;

}

};

</script>
<!-- LOADING SCREEN -->

<div id="loader">

<h1 id="loadingText">DIDDY SUS</h1>

<div id="loadingBar">

<div id="loadingFill"></div>

</div>

</div>

<!-- NAVIGATION -->

<nav>

<a href="#">Home</a>

<a href="#crew">Crew</a>

<a href="#legends">Legends</a>

<a href="#family">Family</a>

<button id="musicButton">🔇 Music</button>

</nav>

<style>

#loader{

position:fixed;

top:0;

left:0;

width:100%;

height:100%;

background:#02040d;

display:flex;

justify-content:center;

align-items:center;

flex-direction:column;

z-index:999999;

transition:1s;

}

#loadingText{

font-family:Orbitron;

font-size:55px;

text-shadow:

0 0 20px cyan,

0 0 60px blue;

margin-bottom:35px;

animation:pulse 1.4s infinite;

}

@keyframes pulse{

50%{

transform:scale(1.05);

}

}

#loadingBar{

width:320px;

height:18px;

background:#111;

border-radius:30px;

overflow:hidden;

}

#loadingFill{

width:0%;

height:100%;

background:linear-gradient(90deg,cyan,blue,purple);

animation:loading 3s forwards;

}

@keyframes loading{

to{

width:100%;

}

}

nav{

position:sticky;

top:0;

display:flex;

justify-content:center;

gap:25px;

padding:18px;

backdrop-filter:blur(12px);

background:rgba(0,0,0,.35);

z-index:1000;

}

nav a{

color:white;

text-decoration:none;

font-family:Orbitron;

transition:.3s;

}

nav a:hover{

color:cyan;

text-shadow:

0 0 10px cyan;

}

#musicButton{

background:rgba(255,255,255,.08);

color:white;

border:1px solid cyan;

padding:10px 18px;

border-radius:10px;

cursor:pointer;

}

.stats{

display:grid;

grid-template-columns:repeat(auto-fit,minmax(200px,1fr));

gap:20px;

margin-top:25px;

}

.stat{

background:rgba(255,255,255,.08);

padding:25px;

border-radius:15px;

text-align:center;

}

.stat h3{

font-size:45px;

color:cyan;

font-family:Orbitron;

}

</style>

<div class="section">

<h2>Legend Statistics</h2>

<div class="stats">

<div class="stat">

<h3 id="wins">0</h3>

<p>Great Memories</p>

</div>

<div class="stat">

<h3 id="hours">0</h3>

<p>Hours Gaming</p>

</div>

<div class="stat">

<h3 id="laughs">0</h3>

<p>Inside Jokes</p>

</div>

<div class="stat">

<h3 id="friends">5</h3>

<p>Legends</p>

</div>

</div>

</div>

<script>

/* LOADER */

window.onload=function(){

setTimeout(function(){

document.getElementById("loader").style.opacity="0";

setTimeout(function(){

document.getElementById("loader").style.display="none";

},1000);

},3200);

};

/* COUNTERS */

function count(id,target){

let number=0;

const speed=target/120;

const timer=setInterval(function(){

number+=speed;

if(number>=target){

number=target;

clearInterval(timer);

}

document.getElementById(id).innerHTML=Math.floor(number);

},15);

}

count("wins",999);

count("hours",4821);

count("laughs",10000);

/* MUSIC BUTTON */

let music=false;

document.getElementById("musicButton").onclick=function(){

music=!music;

this.innerHTML=music?"🔊 Music":"🔇 Music";

alert("Add your favorite song later by placing an MP3 file in the website folder.");

};

</script>
<!-- LOADING SCREEN -->

<div id="loader">

<h1 id="loadingText">DIDDY SUS</h1>

<div id="loadingBar">

<div id="loadingFill"></div>

</div>

</div>

<!-- NAVIGATION -->

<nav>

<a href="#">Home</a>

<a href="#crew">Crew</a>

<a href="#legends">Legends</a>

<a href="#family">Family</a>

<button id="musicButton">🔇 Music</button>

</nav>

<style>

#loader{

position:fixed;

top:0;

left:0;

width:100%;

height:100%;

background:#02040d;

display:flex;

justify-content:center;

align-items:center;

flex-direction:column;

z-index:999999;

transition:1s;

}

#loadingText{

font-family:Orbitron;

font-size:55px;

text-shadow:

0 0 20px cyan,

0 0 60px blue;

margin-bottom:35px;

animation:pulse 1.4s infinite;

}

@keyframes pulse{

50%{

transform:scale(1.05);

}

}

#loadingBar{

width:320px;

height:18px;

background:#111;

border-radius:30px;

overflow:hidden;

}

#loadingFill{

width:0%;

height:100%;

background:linear-gradient(90deg,cyan,blue,purple);

animation:loading 3s forwards;

}

@keyframes loading{

to{

width:100%;

}

}

nav{

position:sticky;

top:0;

display:flex;

justify-content:center;

gap:25px;

padding:18px;

backdrop-filter:blur(12px);

background:rgba(0,0,0,.35);

z-index:1000;

}

nav a{

color:white;

text-decoration:none;

font-family:Orbitron;

transition:.3s;

}

nav a:hover{

color:cyan;

text-shadow:

0 0 10px cyan;

}

#musicButton{

background:rgba(255,255,255,.08);

color:white;

border:1px solid cyan;

padding:10px 18px;

border-radius:10px;

cursor:pointer;

}

.stats{

display:grid;

grid-template-columns:repeat(auto-fit,minmax(200px,1fr));

gap:20px;

margin-top:25px;

}

.stat{

background:rgba(255,255,255,.08);

padding:25px;

border-radius:15px;

text-align:center;

}

.stat h3{

font-size:45px;

color:cyan;

font-family:Orbitron;

}

</style>

<div class="section">

<h2>Legend Statistics</h2>

<div class="stats">

<div class="stat">

<h3 id="wins">0</h3>

<p>Great Memories</p>

</div>

<div class="stat">

<h3 id="hours">0</h3>

<p>Hours Gaming</p>

</div>

<div class="stat">

<h3 id="laughs">0</h3>

<p>Inside Jokes</p>

</div>

<div class="stat">

<h3 id="friends">5</h3>

<p>Legends</p>

</div>

</div>

</div>

<script>

/* LOADER */

window.onload=function(){

setTimeout(function(){

document.getElementById("loader").style.opacity="0";

setTimeout(function(){

document.getElementById("loader").style.display="none";

},1000);

},3200);

};

/* COUNTERS */

function count(id,target){

let number=0;

const speed=target/120;

const timer=setInterval(function(){

number+=speed;

if(number>=target){

number=target;

clearInterval(timer);

}

document.getElementById(id).innerHTML=Math.floor(number);

},15);

}

count("wins",999);

count("hours",4821);

count("laughs",10000);

/* MUSIC BUTTON */

let music=false;

document.getElementById("musicButton").onclick=function(){

music=!music;

this.innerHTML=music?"🔊 Music":"🔇 Music";

alert("Add your favorite song later by placing an MP3 file in the website folder.");

};

</script>
<!-- MEMORY TIMELINE -->

<div class="section">

<h2>📜 Memory Timeline</h2>

<div style="line-height:2;font-size:18px;">

<p>🎮 The squad forms.</p>

<p>😂 The first inside jokes are born.</p>

<p>🏆 Countless games are won.</p>

<p>💀 Gabe finds another way to lose.</p>

<p>🎯 Aiden clutches another Siege round.</p>

<p>🔫 Anthony dominates another shooter.</p>

<p>👑 Sus somehow becomes good at another game.</p>

<p>🧪 Josh walks in with full Rick energy.</p>

<p>❤️ The memories continue.</p>

</div>

</div>

<!-- ENDING -->

<div class="section" style="text-align:center;">

<h2>Thanks For Playing</h2>

<p style="font-size:22px;margin-top:20px;">

No matter what happens in the future, these memories will always exist.

</p>

<p style="margin-top:20px;font-size:20px;color:#72d9ff;">

Anthony • Gabe • Aiden • Josh • Sus

</p>

<button id="creditsButton" style="margin-top:30px;padding:18px 40px;font-size:20px;border:none;border-radius:12px;background:#00bfff;color:white;cursor:pointer;">

Roll Credits

</button>

</div>

<!-- MOVIE CREDITS -->

<div id="credits">

<div id="creditsContent">

<h1>DIDDY SUS</h1>

<br><br>

<h2>Starring</h2>

<p>Aiden</p>

<p>Anthony</p>

<p>Gabe</p>

<p>Josh</p>

<p>Sus</p>

<br><br>

<h2>Favorite Games</h2>

<p>Rainbow Six Siege</p>

<p>Call of Duty</p>

<p>Fortnite</p>

<p>Every Random Game We Found</p>

<br><br>

<h2>Special Thanks</h2>

<p>Every Late Night</p>

<p>Every Laugh</p>

<p>Every Memory</p>

<br><br>

<h1>GGs ❤️</h1>

</div>

</div>

<style>

#credits{

position:fixed;

top:0;

left:0;

width:100%;

height:100%;

background:black;

display:none;

overflow:hidden;

z-index:9999999;

}

#creditsContent{

position:absolute;

width:100%;

text-align:center;

color:white;

font-family:Orbitron,sans-serif;

animation:credits 35s linear forwards;

padding-bottom:300px;

}

@keyframes credits{

0%{

top:100%;

}

100%{

top:-220%;

}

}

</style>

<script>

/* Roll Credits */

document.getElementById("creditsButton").onclick=function(){

document.getElementById("credits").style.display="block";

};

/* Josh Secret */

let joshSecret=0;

const joshCard=document.querySelector("#joshCard");

if(joshCard){

joshCard.onclick=function(){

joshSecret++;

if(joshSecret===7){

alert("🧪 Secret Unlocked!\n\nRick energy levels have reached maximum.");

joshSecret=0;

}

};

}

/* Tiny Fireworks */

function firework(){

const spark=document.createElement("div");

spark.style.position="fixed";

spark.style.left=Math.random()*window.innerWidth+"px";

spark.style.top=Math.random()*window.innerHeight+"px";

spark.style.width="8px";

spark.style.height="8px";

spark.style.borderRadius="50%";

spark.style.background=["cyan","magenta","yellow","lime","orange"][Math.floor(Math.random()*5)];

spark.style.boxShadow="0 0 20px currentColor";

spark.style.pointerEvents="none";

spark.style.zIndex="99999";

document.body.appendChild(spark);

spark.animate([

{transform:"scale(1)",opacity:1},

{transform:"scale(6)",opacity:0}

],{

duration:1000

});

setTimeout(()=>spark.remove(),1000);

}

setInterval(firework,600);

</script>
