<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Creative Student Portfolio</title>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --bg: #0d1425;
  --panel: #182236;
  --green: #d6a6ff;
  --white: #f6f8ff;
  --muted: #9aa7bd;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: Arial, sans-serif;
  background: #060a12;
  color: var(--white);
  line-height: 1.6;
}

a {
  color: inherit;
  text-decoration: none;
}

button {
  font: inherit;
}



nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 22px 6%;
  gap: 20px;
  border-bottom: 1px solid #ffffff0c;
}

.logo {
  font-size: 20px;
  font-weight: 800;
}

.logo span {
  color: var(--green);
}

.nav-links {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  font-size: 12px;
  color: var(--muted);
}

.nav-links a:hover {
  color: var(--green);
}

.hero {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 35px;
  padding: 75px 8% 65px;
}

.eyebrow {
  color: var(--green);
  letter-spacing: 3px;
  text-transform: uppercase;
  font-size: 12px;
  font-weight: bold;
}

h1 {
  font-size: clamp(35px, 5vw, 58px);
  line-height: 1.1;
  margin: 16px 0;
}

h1 span, h2 span {
  color: var(--green);
}

.hero p {
  color: var(--muted);
  font-size: 14px;
  max-width: 450px;
}

.buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 25px;
}

.btn {
  padding: 11px 18px;
  border: 1px solid var(--green);
  border-radius: 5px;
  font-size: 12px;
  cursor: pointer;
  display: inline-block;
}

.btn.primary {
  color: #061b16;
  background: var(--green);
  font-weight: bold;
}

.btn.secondary {
  color: var(--green);
  background: transparent;
}

.profile {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 330px;
}

.orbit {
  position: absolute;
  width: 290px;
  height: 290px;
  border: 1px dashed #31d9a080;
  border-radius: 50%;
  animation: spin 30s linear infinite;
}

.orbit.two {
  width: 340px;
  height: 340px;
  border-color: #ffffff20;
  animation-direction: reverse;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

.photo {
  position: relative;
  z-index: 2;
  width: 230px;
  height: 270px;
  background: var(--green);
  border-radius: 48% 48% 15px 15px;
  overflow: hidden;
  box-shadow: 0 0 50px #31d9a030;
}

.photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.float {
  position: absolute;
  z-index: 3;
  background: var(--panel);
  color: var(--green);
  border: 1px solid #31d9a050;
  padding: 10px 13px;
  border-radius: 10px;
  font-weight: bold;
  font-size: 12px;
}

.f1 { top: 15%; left: 0; }
.f2 { top: 20%; right: 0; }
.f3 { bottom: 12%; left: 6%; }

section {
  padding: 55px 8%;
  border-top: 1px solid #ffffff0c;
}

.section-heading {
  text-align: center;
  margin-bottom: 30px;
}

.section-heading h2 {
  font-size: clamp(25px, 4vw, 35px);
  margin-bottom: 7px;
}

.section-heading p {
  color: var(--muted);
  font-size: 13px;
}

.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}

.card {
  padding: 25px 21px;
  background: var(--panel);
  border: 1px solid #ffffff0d;
  border-radius: 9px;
  transition: .25s;
}

.card:hover {
  transform: translateY(-5px);
  border-color: var(--green);
}

.card.featured {
  background: var(--green);
  color: #09231b;
}

.card-icon {
  font-size: 28px;
  margin-bottom: 15px;
}

.card h3 {
  font-size: 17px;
  margin-bottom: 8px;
}

.card p {
  font-size: 12px;
  color: var(--muted);
}

.card.featured p {
  color: #194c3b;
}

.timeline {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 18px;
}

.timeline-item {
  border-left: 2px solid var(--green);
  padding: 5px 0 8px 18px;
}

.timeline-item small {
  color: var(--green);
  font-size: 11px;
}

.timeline-item h3 {
  font-size: 15px;
  margin: 6px 0;
}

.timeline-item p {
  font-size: 12px;
  color: var(--muted);
}

.process {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.process-item {
  padding: 15px 0;
}

.number {
  width: 40px;
  height: 40px;
  display: grid;
  place-items: center;
  background: var(--green);
  color: #09231b;
  font-weight: bold;
  border-radius: 8px;
  margin-bottom: 12px;
}

.process-item h3 {
  font-size: 14px;
  margin-bottom: 5px;
}

.process-item p {
  color: var(--muted);
  font-size: 12px;
}

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 35px;
  align-items: center;
}

.about-grid img {
  width: 100%;
  height: 240px;
  object-fit: cover;
  border-radius: 9px;
}

.about-grid p {
  color: var(--muted);
  font-size: 13px;
  margin-top: 12px;
}

.skills {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}

.skill {
  text-align: center;
}

.circle {
  --percent: 80%;
  width: 105px;
  height: 105px;
  margin: 0 auto 15px;
  border-radius: 50%;
  background: conic-gradient(
    var(--green) var(--percent),
    #283349 var(--percent)
  );
  display: grid;
  place-items: center;
  position: relative;
}

.circle::before {
  content: "";
  position: absolute;
  inset: 7px;
  background: var(--bg);
  border-radius: 50%;
}

.circle strong {
  position: relative;
  font-size: 20px;
}

.skill h3 {
  font-size: 14px;
}

.skill p {
  color: var(--muted);
  font-size: 11px;
  margin-top: 5px;
}

.contact {
  text-align: center;
  background: #121c2e;
}

.contact p {
  color: var(--muted);
  margin: 10px 0 20px;
  font-size: 13px;
}

footer {
  text-align: center;
  padding: 20px;
  color: var(--muted);
  font-size: 11px;
}

footer span {
  color: var(--green);
}

@media(max-width: 750px) {
  .hero, .about-grid {
    grid-template-columns: 1fr;
  }

  .hero {
    text-align: center;
    padding: 45px 7%;
  }

  .hero p {
    margin: auto;
  }

  .buttons {
    justify-content: center;
  }

  .profile {
    margin-top: 25px;
  }

  .cards {
    grid-template-columns: 1fr;
  }

  .timeline {
    grid-template-columns: 1fr;
  }

  .nav-links {
    gap: 10px;
  }

  nav {
    align-items: flex-start;
    flex-direction: column;
  }

  .process {
    grid-template-columns: 1fr 1fr;
  }
}

@media(max-width: 420px) {
  .skills {
    grid-template-columns: repeat(2, 1fr);
  }

  .process {
    grid-template-columns: 1fr;
  }
}

@media print {
  @page {
    size: A4;
    margin: 10mm;
  }

  body {
    background: white;
    print-color-adjust: exact;
    -webkit-print-color-adjust: exact;
  }

  .page {
    width: 100%;
    margin: 0;
    border: 0;
    box-shadow: none;
  }

  nav .nav-links, .buttons {
    display: none;
  }

  nav, section, .hero {
    padding: 22px 5%;
  }

  .hero {
    grid-template-columns: 1fr 1fr;
  }

  .card, .timeline-item, .skill {
    break-inside: avoid;
  }

  a {
    text-decoration: none;
  }
}
</style>
</head>

<body>
<div class="page">

<nav>
  <div class="nav-links">
    <a href="#home">Home</a>
    <a href="#services">Skills</a>
    <a href="#education">Education</a>
    <a href="#projects">Projects</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<!-- HERO -->
<div class="hero" id="home">
  <div>
    <div class="eyebrow">Hello, welcome to my world</div>
    <h1>I'm <span>R.Harini</span>
    <p>
      I am a college student passionate about technology,
      web development and creative problem-solving.
      I love turning new ideas into useful digital experiences.
    </p>
    <div class="buttons">
      <a class="btn primary" href="#projects">Explore My Work ↗</a>
      <a class="btn secondary"
      href="#contact">8248604656</a>
    </div>
  </div>

  <div class="profile">
    <div class="orbit"></div>
    <div class="orbit two"></div>

    <div class="photo">
      <!-- Change to your own photo file -->
       <div class="photo">
  <img
      src="https://i.ibb.co/c0P67sM/Whats-App-Image-2026-10-11-at-11-47-35-PM.jpg" alt="Whats App Image 2026 10 11 at 11 47 35 PM" border="0"></a>
    alt="My Photo"
    onerror="this.style.display='none'; this.parentElement.style.background='#31d9a0'; this.parentElement.innerHTML='<div style=&quot;color:#09231b;padding:75px 10px;text-align:center;font-weight:bold&quot;>ADD YOUR PHOTO HERE</div>';"
  >
</div>
           onerror="this.style.display='none';
           this.parentElement.style.background='#31d9a0';
           this.parentElement.innerHTML=
           '<div style=&quot;color:#09231b;padding:75px 10px;text-align:center;font-weight:bold&quot;>ADD YOUR<br>PHOTO HERE</div>';">
    </div> 
  <div class="float f1">✦ Creative</div>
    <div class="float f2">⌘ Developer</div>
    <div class="float f3">✧ Learner</div>
  </div>
</div>

<!-- SERVICES / SKILLS -->
<section id="services">
  <div class="section-heading">
    <div class="eyebrow">What I Do</div>
    <h2>My <span>Skills & Interests</span></h2>
    <p>Things I enjoy learning and creating.</p>
  </div>

  <div class="cards">
    <div class="card">
      <div class="card-icon">⌘</div>
      <h3>Web Development</h3>
      <p>Creating responsive web pages using HTML, CSS and JavaScript.</p>
    </div>

    <div class="card featured">
      <div class="card-icon">✳</div>
      <h3>Creative Design</h3>
      <p>Exploring modern layouts, colors, user interfaces and visual ideas.</p>
    </div>

    <div class="card">
      <div class="card-icon">⌘</div>
      <h3>Programming</h3>
      <p>Learning programming and building useful beginner projects.</p>
    </div>
  </div>
</section>

<!-- EDUCATION & EXPERIENCE -->
<section id="education">
  <div class="section-heading">
    <div class="eyebrow">My Journey</div>
    <h2>Education <span>& Experience</span></h2>
  </div>

  <div class="timeline">
    <div class="timeline-item">
      <small>2025-2029</small>
      <h3>B.Tech CSE DS(AI)</h3>
      <p>Dr. M.G.R. Educational and Research Institute</p>
      <p> department:Data Science and Artificial interlligence</p>
    </div>

    <div class="timeline-item">
      <small>PROJECT EXPERIENCE</small>
      <h3>Student Web Designer</h3>
      <p>Designed personal web pages and practiced frontend development.</p>
    </div>

    <div class="timeline-item">
      <small>2025-2029</small>
      <h3>Higher Secondary Education</h3>
      <p>saratha vidhyala girls higher secondary school.</p>
    </div>

    <div class="timeline-item">
      <small>CONTINUOUS LEARNING</small>
      <h3>Technical Skills</h3>
      <p>Learning programming, web development and digital tools.</p>
    </div>
  </div>
</section>

<!-- WORK PROCESS -->
<section>
  <div class="section-heading">
    <div class="eyebrow">How I Learn</div>
    <h2>My <span>Work Process</span></h2>
    <p>A simple approach to creating better projects.</p>
  </div>

  <div class="process">
    <div class="process-item">
      <div class="number">01</div>
      <h3>Research</h3>
      <p>Understand the problem and explore possible solutions.</p>
    </div>

    <div class="process-item">
      <div class="number">02</div>
      <h3>Plan & Design</h3>
      <p>Organize ideas and create a clear design.</p>
    </div>

    <div class="process-item">
      <div class="number">03</div>
      <h3>Develop</h3>
      <p>Build the project and test its functionality.</p>
    </div>

    <div class="process-item">
      <div class="number">04</div>
      <h3>Improve</h3>
      <p>Fix problems and refine the final result.</p>
    </div>

    <div class="process-item">
      <div class="number">05</div>
      <h3>Present</h3>
      <p>Showcase the completed work clearly.</p>
    </div>

    <div class="process-item">
      <div class="number">06</div>
      <h3>Keep Learning</h3>
      <p>Use feedback to learn new skills and improve.</p>
    </div>
  </div>
</section>

<!-- ABOUT -->

    <div style="text-align:center;">
  <div class="eyebrow">A Little About Me</div>

  <h2 style="font-size:30px; margin-top:10px;">
    Learn. Create. <span>Grow.</span>
  </h2>
</div>
     <p style="text-align:center;">
  I am a student who enjoys exploring technology,
  developing practical skills and trying creative ideas.
  My goal is to gain experience, build meaningful projects
  and continue improving every day.
</p>

<p style="text-align:center;">
  I value teamwork, curiosity, consistency and learning
  through practical experience.
</p>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-heading">
    <h2>Featured <span>Projects</span></h2>
    <p>Replace these examples with your actual projects.</p>
  </div>

  <div class="cards">
    <div class="card">
      <div class="card-icon">🌐</div>
      <h3>Portfolio Website</h3>
      <p>A responsive personal website built with HTML and CSS.</p>
    </div>

    <div class="card">
      <div class="card-icon">🧮</div>
      <h3>Student Calculator</h3>
      <p>A beginner-friendly Python application for calculations.</p>
    </div>

    <div class="card">
      <div class="card-icon">💡</div>
      <h3>My Next Idea</h3>
      <p>Describe an original project you are developing or planning.</p>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section>
  <div class="section-heading">
    <div class="eyebrow">What I'm Learning</div>
    <h2>My <span>Technical Skills</span></h2>
  </div>

  <div class="skills">
    <div class="skill">
      <div class="circle" style="--percent:80%">
        <strong>80%</strong>
      </div>
      <h3>HTML & CSS</h3>
      <p>Web page design</p>
    </div>

    <div class="skill">
      <div class="circle" style="--percent:65%">
        <strong>65%</strong>
      </div>
      <h3>Python</h3>
      <p>Programming</p>
    </div>

    <div class="skill">
      <div class="circle" style="--percent:70%">
        <strong>70%</strong>
      </div>
      <h3>C Programming</h3>
      <p>Programming basics</p>
    </div>

    <div class="skill">
      <div class="circle" style="--percent:60%">
        <strong>60%</strong>
      </div>
      <h3>JavaScript</h3>
      <p>Frontend basics</p>
    </div>

    <div class="skill">
      <div class="circle" style="--percent:75%">
        <strong>70%</strong>
      </div>
      <h3>Communication</h3>
      <p>Team collaboration</p>
    </div>

    <div class="skill">
      <div class="circle" style="--percent:85%">
        <strong>85%</strong>
      </div>
      <h3>Problem Solving</h3>
      <p>Analytical thinking</p>
    </div>
  </div>
</section>

<!-- CONTACT -->


</div>
</body>
</html>
i
