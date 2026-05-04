<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Shreyas JM | AI & FinTech Engineer</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">
<link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">

<style>
html { scroll-behavior: smooth; }

body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: black;
  color: white;
}

#progress {
  position: fixed;
  top: 0;
  left: 0;
  height: 4px;
  background: linear-gradient(90deg, #3b82f6, #9333ea);
  width: 0%;
  z-index: 999;
}

section { padding: 80px 20px; text-align: center; }

h1 { font-size: 3rem; }
h2 { font-size: 2rem; }

.btn {
  padding: 10px 20px;
  border-radius: 20px;
  text-decoration: none;
  color: white;
  border: 1px solid white;
  margin: 5px;
}

.btn-primary {
  background: linear-gradient(45deg, #3b82f6, #9333ea);
  border: none;
}

.grid { display: grid; gap: 20px; }

@media(min-width:768px){
  .grid-3 { grid-template-columns: repeat(3,1fr); }
}

.card {
  background: rgba(255,255,255,0.05);
  padding: 20px;
  border-radius: 15px;
  transition: 0.3s;
}

.card:hover {
  transform: translateY(-10px) scale(1.03);
  box-shadow: 0 0 25px rgba(147,51,234,0.5);
}

.tags span {
  background: rgba(59,130,246,0.2);
  padding: 5px 10px;
  border-radius: 10px;
  margin: 3px;
  display: inline-block;
  font-size: 12px;
}

.chatbox {
  max-width: 400px;
  margin: auto;
  background: #111;
  padding: 10px;
  border-radius: 10px;
  height: 250px;
  overflow-y: auto;
  text-align: left;
}

input { padding:10px; width:65%; border-radius:10px; border:none; }
button { padding:10px; border-radius:10px; border:none; background:#3b82f6; color:white; }

</style>
</head>

<body>

<div id="progress"></div>

<!-- HERO -->
<section>
  <h1>Shreyas JM</h1>
  <p>Building AI-powered financial systems & data-driven solutions</p>
  <a href="#projects" class="btn btn-primary">View Projects</a>
</section>

<!-- ABOUT -->
<section>
  <h2>About Me</h2>
  <p>
    AI & FinTech Engineer focused on building intelligent systems using
    machine learning, real-time data, and automation.
  </p>
</section>

<!-- IMPACT -->
<section>
  <h2>Impact</h2>
  <div class="grid grid-3">
    <div class="card"><h1>5+</h1><p>Projects</p></div>
    <div class="card"><h1>3+</h1><p>Domains</p></div>
    <div class="card"><h1>100%</h1><p>Real-world Focus</p></div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <h2>Projects</h2>

  <div class="grid grid-3">

    <div class="card">
      <h3>🤖 AI Financial Analyst</h3>
      <p>ML-based stock prediction system</p>
      <div class="tags">
        <span>Python</span><span>ML</span><span>LSTM</span>
      </div>
      <a href="#" class="btn btn-primary">Live</a>
    </div>

    <div class="card">
      <h3>📊 Crypto Analyzer</h3>
      <p>Real-time crypto dashboard</p>
      <div class="tags">
        <span>API</span><span>JS</span>
      </div>
    </div>

    <div class="card">
      <h3>🌐 Cloud Portfolio</h3>
      <p>LinkedIn → Portfolio system</p>
      <a href="https://www.zapfolio.in/jmshreyas882000-cloud" target="_blank" class="btn">View</a>
    </div>

  </div>
</section>

<!-- CHATBOT -->
<section>
  <h2>Ask Me 🤖</h2>
  <div class="chatbox" id="chatbox"></div>
  <br>
  <input id="input" placeholder="Ask something..." />
  <button onclick="sendMessage()">Send</button>
</section>

<!-- GITHUB -->
<section>
  <h2>GitHub</h2>
  <img src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=radical">
</section>

<!-- CONTACT -->
<section>
  <h2>Contact</h2>
  <a href="mailto:jmshreyas882000@gmail.com" class="btn btn-primary">Email</a>
  <a href="https://www.linkedin.com/in/shreyas-jm-43850b261/" class="btn">LinkedIn</a>
</section>

<footer style="padding:20px;color:gray;">© 2026 Shreyas JM</footer>

<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>

<script>
AOS.init();

// scroll bar
window.onscroll = () => {
  let s = document.documentElement.scrollTop;
  let h = document.documentElement.scrollHeight - document.documentElement.clientHeight;
  document.getElementById("progress").style.width = (s/h)*100 + "%";
};

// chatbot (simple for now)
function sendMessage(){
  const input = document.getElementById("input");
  const chat = document.getElementById("chatbox");

  if(!input.value) return;

  chat.innerHTML += `<p style="color:#3b82f6">${input.value}</p>`;
  chat.innerHTML += `<p>I'm Shreyas's AI assistant. Backend coming soon.</p>`;

  input.value="";
  chat.scrollTop = chat.scrollHeight;
}
</script>

</body>
</html>
