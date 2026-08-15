<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jensen.exe — Happy Sweet 16</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Georgia,serif;
font-style:italic;
}

body{
background:#001b33;
color:#d7f8ff;
overflow:hidden;
}

#boot{
position:fixed;
inset:0;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
background:linear-gradient(180deg,#001b33,#004b87);
text-align:center;
z-index:999;
}

#boot h1{
font-size:2.4rem;
text-shadow:0 0 15px cyan;
}

#desktop{
display:none;
height:100vh;
overflow:auto;
padding:20px;
background:
linear-gradient(rgba(0,0,0,.2),rgba(0,0,0,.2)),
radial-gradient(circle,#005fa3,#00264d);
}

.window{
max-width:760px;
margin:auto;
background:rgba(8,25,46,.9);
border:2px solid #66d9ff;
border-radius:14px;
box-shadow:0 0 25px rgba(0,255,255,.3);
overflow:hidden;
}

.titlebar{
background:linear-gradient(90deg,#0a5ea8,#2bb7ff);
padding:10px;
text-align:center;
color:white;
}

.content{
padding:22px;
}

h2{
font-size:2.5rem;
text-align:center;
text-shadow:0 0 12px cyan;
margin-bottom:12px;
}

img{
width:100%;
border-radius:14px;
border:2px solid #66d9ff;
margin:18px 0;
}

.grid{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:12px;
margin:20px 0;
}

.icon{
background:#003d66;
border:1px solid #66d9ff;
border-radius:10px;
padding:16px;
text-align:center;
cursor:pointer;
transition:.2s;
}

.icon:hover{
transform:scale(1.05);
box-shadow:0 0 12px cyan;
}

.popup{
position:fixed;
inset:0;
display:none;
justify-content:center;
align-items:center;
background:rgba(0,0,0,.6);
}

.box{
background:#002845;
padding:22px;
border-radius:12px;
border:2px solid #66d9ff;
max-width:330px;
text-align:center;
}

button{
margin-top:14px;
padding:10px 18px;
border:none;
border-radius:999px;
background:#66d9ff;
color:#002845;
font-size:1rem;
}

.crt{
position:fixed;
inset:0;
pointer-events:none;
background:repeating-linear-gradient(
0deg,
rgba(255,255,255,.03) 0px,
rgba(255,255,255,.03) 2px,
transparent 4px
);
opacity:.35;
}
</style>
</head>

<body>

<div class="crt"></div>

<div id="boot">
<h1>✦ booting jensen.exe ✦</h1>
<p id="bootText">checking tea supplies...</p>
<p id="percent">0%</p>
</div>

<div id="desktop">

<div class="window">

<div class="titlebar">
💻 windows xp • tumblr edition • jensen.exe
</div>

<div class="content">

<h2>happy sweet sixteen, jensen ♡</h2>

<img src="YOUR_JENSEN_PHOTO_URL" alt="Jensen">

<p>dear jensen,</p>

<p>happy 16th!! i hope this year gives you ridiculous amounts of laughter, chaotic online memories, immaculate playlists, and enough confidence to keep being unapologetically yourself.</p>

<p><b>it's completely alright to be gay.</b> (i'm still legally obligated to call you gay because it's funny. 😭)</p>

<p>also... you're british. which means i'm assuming you've already had approximately <b>17 cups of tea</b> today and politely apologized to the kettle for making it work overtime. ☕</p>

<p>may your wifi stay fast, your hair keep serving, and your tea never be lukewarm... because i'm pretty sure that's considered a national emergency over there.</p>

<p>thank you for being such a chaotic online friend. here's to more random conversations, dumb jokes, and bullying your tea addiction forever. ♡</p>

<div class="grid">

<div class="icon" onclick="tea()">
☕<br>Tea.exe
</div>

<div class="icon" onclick="gay()">
🌈<br>Gay_Detector.exe
</div>

<div class="icon" onclick="cert()">
📜<br>British_Certificate
</div>

<div class="icon" onclick="wish()">
🎂<br>Birthday_Surprise
</div>

</div>

</div>

</div>

</div>

<div class="popup" id="popup">
<div class="box">
<p id="popupText"></p>
<button onclick="closePop()">close ✧</button>
</div>
</div>

<script>
const msgs=[
"checking tea supplies...",
"detecting britishness... 100% 🇬🇧",
"locating kettle...",
"loading tumblr glitter...",
"finding emotional support teacup...",
"system approved."
];

let i=0,p=0;

const t=setInterval(()=>{
document.getElementById("bootText").innerHTML=msgs[Math.min(i,msgs.length-1)];
document.getElementById("percent").innerHTML=p+"%";
i++;
p+=20;

if(p>100){
clearInterval(t);
document.getElementById("boot").style.display="none";
document.getElementById("desktop").style.display="block";
document.body.style.overflow="auto";
}
},600);

function pop(x){
document.getElementById("popupText").innerHTML=x;
document.getElementById("popup").style.display="flex";
}

function closePop(){
document.getElementById("popup").style.display="none";
}

function tea(){
pop("☕ Tea.exe<br><br>Tea Level: 9000%.<br>You've consumed approximately 47 cups today. Please hydrate. The kettle misses you.");
}

function gay(){
pop("🌈 Gay_Detector.exe<br><br>Results: It's completely alright to be gay. System Approved. 😭");
}

function cert(){
pop("📜 Official British Certification<br><br>Tea addiction: 100%<br>Saying 'cheers mate': Detected<br>Apologizing to the kettle: Confirmed<br>Beans on toast: Under investigation.");
}

function wish(){
pop("🎂 Happy Sweet 16, Jensen!!<br><br>Now go make a wish... and then put the kettle on. ☕");
}

document.addEventListener("keydown",e=>{
if(e.key.toLowerCase()=="o"){
pop("🇬🇧 British Mode Activated.");
}
});
</script>

</body>
</html>
