# tnpacao

<!DOCTYPE html>
<html>
  <head>
   <meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Trexielyn Pacao| Portfolio CV</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
    scroll-behavior:smooth;
}

body{
    background: radial-gradient(circle at top, #120018, #05050a);
    color:white;
}

/* HERO */
header{
    height:100vh;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    background: linear-gradient(135deg,#1a001f,#2b0a3d,#ff4fd8);
    position:relative;
    overflow:hidden;
}

/* glowing background effect */
header::before{
    content:"";
    position:absolute;
    width:400px;
    height:400px;
    background:#ff4fd8;
    filter:blur(120px);
    opacity:0.3;
    top:-100px;
    left:-100px;
}

header::after{
    content:"";
    position:absolute;
    width:300px;
    height:300px;
    background:#ff2cc3;
    filter:blur(120px);
    opacity:0.25;
    bottom:-80px;
    right:-80px;
}

.profile{
    width:110px;
    height:110px;
    border-radius:50%;
    background:#ff4fd8;
    color:white;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:38px;
    font-weight:bold;
    box-shadow:0 0 30px #ff4fd8;
    z-index:1;
}

h1{
    font-size:3rem;
    margin-top:15px;
    z-index:1;
}

.typing-container{
    margin-top:10px;
    font-size:1.2rem;
    color:#ffb3ea;
    min-height:30px;
    z-index:1;
}

.cursor{
    animation:blink 0.7s infinite;
}

@keyframes blink{
    50%{opacity:0;}
}

header p{
    margin-top:10px;
    opacity:0.8;
    z-index:1;
}

.btn{
    margin-top:20px;
    padding:12px 25px;
    background:#ff4fd8;
    color:white;
    border-radius:30px;
    text-decoration:none;
    font-weight:600;
    box-shadow:0 0 20px #ff4fd8;
    transition:0.3s;
    z-index:1;
}

.btn:hover{
    transform:scale(1.08);
    box-shadow:0 0 30px #ff4fd8;
}

/* NAV */
nav{
    position:sticky;
    top:0;
    background:rgba(0,0,0,0.7);
    backdrop-filter:blur(10px);
    display:flex;
    justify-content:center;
    padding:12px;
    z-index:100;
}

nav a{
    color:white;
    text-decoration:none;
    margin:0 12px;
    transition:0.3s;
    font-size:14px;
}

nav a:hover{
    color:#ff4fd8;
}

/* SECTIONS */
section{
    max-width:900px;
    margin:50px auto;
    padding:25px;
    background:rgba(255,255,255,0.05);
    border:1px solid rgba(255,79,216,0.2);
    border-radius:15px;
    backdrop-filter:blur(10px);
    box-shadow:0 0 25px rgba(255,79,216,0.1);
    opacity:0;
    transform:translateY(30px);
    animation:fadeUp 1s forwards;
}

@keyframes fadeUp{
    to{
        opacity:1;
        transform:translateY(0);
    }
}

h2{
    color:#ff4fd8;
    margin-bottom:15px;
    border-left:4px solid #ff4fd8;
    padding-left:10px;
}

.card{
    background:rgba(255,255,255,0.06);
    padding:15px;
    border-radius:10px;
    margin-bottom:10px;
    border-left:3px solid #ff4fd8;
}

/* FOOTER */
footer{
    text-align:center;
    padding:20px;
    background:black;
    margin-top:40px;
    font-size:13px;
    opacity:0.7;
}
</style>
</head>

<body>

<header>
    <div class="profile">TP</div>
    <h1>Trexielyn Pacao</h1>

    <div class="typing-container">
        <span id="typed"></span><span class="cursor">|</span>
    </div>

    <p>BS Information Technology | Fresh Graduate</p>
    <a class="btn" href="#" onclick="downloadResume()">Download Resume</a>
</header>

<nav>
    <a href="#objective">Objective</a>
    <a href="#education">Education</a>
    <a href="#experience">Experience</a>
    <a href="#skills">Skills</a>
    <a href="#contact">Contact</a>
</nav>

<section id="objective">
    <h2>Career Objective</h2>
    <p>
        Motivated BS Information Technology graduate seeking an entry-level IT position.
        Passionate about web development, problem solving, and building modern digital solutions.
    </p>
</section>

<section id="education">
    <h2>Education</h2>
    <div class="card">
        BS Information Technology<br>
        Pateros Technological College<br>
        2026
    </div>
</section>

<section id="experience">
    <h2>Experience</h2>
    <div class="card">
        IT Intern (OJT) - Assisted in troubleshooting systems and software installation.
    </div>
</section>

<section id="skills">
    <h2>Skills</h2>
    <div class="card">
        HTML • CSS • JavaScript • Troubleshooting • MS Office • Teamwork
    </div>
</section>

<section id="contact">
    <h2>Contact</h2>
    <div class="card">
        Email: trexielyn@email.com<br>
        Phone: 09621021694<br>
        Location: Philippines
    </div>
</section>

<footer>
    © 2026 Trexielyn Pacao | Portfolio CV
</footer>

<script>
// typing animation
const words = [
    "IT Student...",
    "Future Web Developer...",
    "UI Designer...",
    "Problem Solver..."
];

let i = 0;
let j = 0;
let current = "";
let deleting = false;

function type(){
    current = words[i];

    if(!deleting){
        document.getElementById("typed").textContent = current.substring(0,j++);
        if(j > current.length){
            deleting = true;
            setTimeout(type, 1000);
            return;
        }
    } else {
        document.getElementById("typed").textContent = current.substring(0,j--);
        if(j < 0){
            deleting = false;

type();

// download resume
function downloadResume(){
    const text = `
Trexielyn Pacao
BS Information Technology

Skills: HTML, CSS, JavaScript
Objective: Entry-level IT position
    `;

    const blob = new Blob([text], {type:"text/plain"});
    const a = document.createElement("a");
    a.href = URL.createObjectURL(blob);
    a.download = "Trexielyn_Pacao_CV.txt";
    a.click();
}
</script>

</body>
</html>            i = (i+1) % words.length;
        }
    }

    setTimeout(type, deleting ? 60 : 90);
}
