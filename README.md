<!DOCTYPE html>
<html>
<head>
<title>Message</title>

<style>

body{
margin:0;
background: linear-gradient(135deg,#1f0036,#5b0060,#a1006b);
color:white;
font-family:Arial, sans-serif;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
text-align:center;
overflow:hidden;
}

/* floating particles */

body::before{
content:"";
position:absolute;
width:200%;
height:200%;
background-image:radial-gradient(white 1px, transparent 1px);
background-size:50px 50px;
opacity:0.15;
animation:moveStars 60s linear infinite;
}

@keyframes moveStars{
from{transform:translateY(0);}
to{transform:translateY(-500px);}
}

/* pages */

.page{
position:absolute;
max-width:800px;
padding:40px;
opacity:0;
transform:translateY(20px);
transition:opacity 1s ease, transform 1s ease;
pointer-events:none;
}

.page.active{
opacity:1;
transform:translateY(0);
pointer-events:auto;
}

/* arrow */

.arrow{
font-size:60px;
cursor:pointer;
margin-top:20px;
animation:bounce 1.5s infinite;
}

@keyframes bounce{
0%,100%{transform:translateY(0);}
50%{transform:translateY(12px);}
}

p{
font-size:18px;
line-height:1.7;
}

/* button */

button{
margin-top:40px;
padding:12px 30px;
font-size:18px;
border:none;
border-radius:6px;
cursor:pointer;
background:white;
}

/* glowing text */

.glow{
font-size:60px;
text-shadow:
0 0 10px white,
0 0 20px white,
0 0 30px #ff4d4d,
0 0 40px #ff4d4d,
0 0 50px #ff4d4d;
animation:glow 2s infinite alternate;
}

@keyframes glow{
from{ text-shadow:0 0 10px white;}
to{ text-shadow:0 0 40px #ff4d4d;}
}

</style>
</head>

<body>

<!-- PAGE 1 -->

<div class="page active" id="page1">

<h1>I wanna say something to you</h1>

<div class="arrow" onclick="nextPage(2)">⬇</div>

</div>


<!-- PAGE 2 -->

<div class="page" id="page2">

<p>
See aratrika ik I had said soo many wrong things to you cause at that time I was depressed because of all those things which happen to you bec of me and I was really depressed and sad still all those things haunt me and I can't forgot what others said to you and disrespected you in a way which I had never imagine that gonna happen to you bec of me and u have to hear soo many things which are against me and gonna make u feel bad Rn ik I made many many mistakes of saying all those things to you when I was telling you that we should broke up I said all that only bec I was depressed and second ki I don't want that I treat you in that way even I never knew why u loved me or chose me over soo many boys even if you had many different choice and ehan too but still u chose me over all of them I am glad that I was ur bf but that not the point The point is I want you say sorry to you for the things that I said when we are breaking up and all the things which made u think bad abt me Right now idk what's going on ur mind and what will be ur reaction when u gonna read this But all I wanna say is a sorry bec that's all in can If i would be there in kolkata i will kneel down in front of you and say apologize for every single mistake that I had made during our relationship honestly saying I miss our relationship soo much and misses you too But i fear relationships now cause I don't want that the other person gets disrespected Or need to hear soo many bad things Abt himself All i wanted is to treat you the way u want every single moment of your life give u the love u deserve and try to treat u in the much better way as ur family treated you But in all those things I failed. I am sorry for everything aratrika Really sorry
</p>

<button onclick="nextPage(3)">Continue</button>

</div>


<!-- PAGE 3 -->

<div class="page" id="page3">

<h1 class="glow">I am sorry Aratrika</h1>

</div>


<script>

function nextPage(pageNumber){

document.querySelectorAll(".page").forEach(p=>{
p.classList.remove("active");
});

document.getElementById("page"+pageNumber).classList.add("active");

}

</script>

</body>
</html>
