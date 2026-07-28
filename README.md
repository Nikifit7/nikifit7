<!--
  README.md - Monique Navarro
  Full Stack Developer | Green Tech | ESG | OT/IT Integration
-->

<style>
  /* ===== BASE & RESET ===== */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    background: #0a0a1a;
    overflow-x: hidden;
    font-family: 'Courier New', monospace;
  }

  /* ===== SPACE BACKGROUND ===== */
  .space-background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: radial-gradient(ellipse at bottom, #1B2735 0%, #090A0F 100%);
    z-index: -2;
  }

  .stars-layer {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    pointer-events: none;
  }

  .star-bg {
    position: absolute;
    background: white;
    border-radius: 50%;
    animation: twinkle var(--duration) ease-in-out infinite alternate;
  }

  @keyframes twinkle {
    0% { opacity: 0.2; transform: scale(0.8); }
    100% { opacity: 1; transform: scale(1.2); }
  }

  /* ===== ASTRONAUT & STARS FROM UIVERSE ===== */
  @keyframes snow {
    0% { opacity: 0; transform: translateY(0px); }
    20% { opacity: 1; }
    100% { opacity: 1; transform: translateY(650px); }
  }

  @keyframes astronaut {
    0% { transform: rotate(0deg) scale(1); }
    50% { transform: rotate(180deg) scale(1.1); }
    100% { transform: rotate(360deg) scale(1); }
  }

  @keyframes float {
    0%, 100% { transform: translateY(0px) rotate(0deg); }
    50% { transform: translateY(-20px) rotate(5deg); }
  }

  .box-of-star1,
  .box-of-star2,
  .box-of-star3,
  .box-of-star4 {
    width: 100%;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    height: 700px;
    pointer-events: none;
  }

  .box-of-star1 { animation: snow 5s linear infinite; }
  .box-of-star2 { animation: snow 5s -1.64s linear infinite; }
  .box-of-star3 { animation: snow 5s -2.30s linear infinite; }
  .box-of-star4 { animation: snow 5s -3.30s linear infinite; }

  .star {
    width: 3px;
    height: 3px;
    border-radius: 50%;
    background-color: #FFF;
    position: absolute;
    z-index: 1;
    opacity: 0.7;
    box-shadow: 0 0 10px rgba(255,255,255,0.5);
  }

  .star:before {
    content: "";
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background-color: #FFF;
    position: absolute;
    top: 80px;
    left: 70px;
    opacity: .7;
    box-shadow: 0 0 15px rgba(255,255,255,0.3);
  }

  .star:after {
    content: "";
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background-color: #FFF;
    position: absolute;
    top: 8px;
    left: 170px;
    opacity: .9;
    box-shadow: 0 0 20px rgba(255,255,255,0.4);
  }

  .star-position1 { top: 30px; left: 20px; }
  .star-position2 { top: 110px; left: 250px; }
  .star-position3 { top: 60px; left: 570px; }
  .star-position4 { top: 120px; left: 900px; }
  .star-position5 { top: 20px; left: 1120px; }
  .star-position6 { top: 90px; left: 1280px; }
  .star-position7 { top: 30px; left: 1480px; }

  .astronaut-container {
    position: fixed;
    right: 50px;
    bottom: 50px;
    z-index: 10;
    animation: float 6s ease-in-out infinite;
    filter: drop-shadow(0 0 30px rgba(0, 212, 255, 0.3));
  }

  .astronaut {
    width: 200px;
    height: 250px;
    position: relative;
    animation: astronaut 8s linear infinite;
    transform-origin: center center;
  }

  .schoolbag {
    width: 80px;
    height: 120px;
    position: absolute;
    z-index: 1;
    top: calc(50% - 60px);
    left: calc(50% - 40px);
    background: linear-gradient(135deg, #6e8efb, #a777e3);
    border-radius: 50px 50px 0 0 / 30px 30px 0 0;
    box-shadow: inset 0 -20px 30px rgba(0,0,0,0.2);
  }

  .head {
    width: 77px;
    height: 64px;
    position: absolute;
    z-index: 3;
    background: linear-gradient(135deg, #e3e8eb 0%, #fbfdfa 100%);
    border-radius: 50%;
    top: 27px;
    left: calc(50% - 38.5px);
    box-shadow: 0 0 30px rgba(255,255,255,0.1);
  }

  .head:after {
    content: "";
    width: 48px;
    height: 40px;
    position: absolute;
    top: calc(50% - 20px);
    left: calc(50% - 24px);
    background: linear-gradient(180deg, #15aece 0%, #0391bf 100%);
    border-radius: 15px;
    box-shadow: inset 0 -5px 15px rgba(0,0,0,0.2);
  }

  .head:before {
    content: "";
    width: 10px;
    height: 20px;
    position: absolute;
    top: calc(50% - 10px);
    left: -3px;
    background-color: #618095;
    border-radius: 5px;
    box-shadow: 73px 0px 0px #618095;
  }

  .body {
    width: 68px;
    height: 80px;
    position: absolute;
    z-index: 2;
    background: linear-gradient(135deg, #e3e8eb 0%, #fbfdfa 100%);
    border-radius: 40px / 20px;
    top: 84px;
    left: calc(50% - 33px);
    box-shadow: inset 0 -10px 20px rgba(0,0,0,0.1);
  }

  .panel {
    width: 48px;
    height: 32px;
    position: absolute;
    top: 16px;
    left: calc(50% - 24px);
    background: linear-gradient(135deg, #6e8efb, #a777e3);
    border-radius: 10px;
    box-shadow: 0 0 20px rgba(110, 142, 251, 0.3);
  }

  .panel:before {
    content: "";
    width: 24px;
    height: 4px;
    position: absolute;
    top: 7px;
    left: 5px;
    background-color: #fbfdfa;
    border-radius: 2px;
    box-shadow: 0px 7px 0px #fbfdfa, 0px 14px 0px #fbfdfa;
  }

  .panel:after {
    content: "";
    width: 6px;
    height: 6px;
    position: absolute;
    top: 7px;
    right: 5px;
    background-color: #fbfdfa;
    border-radius: 50%;
    box-shadow: 0px 11px 0px 2px #fbfdfa;
  }

  .arm {
    width: 64px;
    height: 24px;
    position: absolute;
    top: 97px;
    z-index: 2;
  }

  .arm-left {
    left: 24px;
    background: linear-gradient(135deg, #e3e8eb, #d0d5d8);
    border-radius: 0 0 0 39px;
  }

  .arm-right {
    right: 24px;
    background: linear-gradient(135deg, #fbfdfa, #e8eaec);
    border-radius: 0 0 39px 0;
  }

  .arm-left:before,
  .arm-right:before {
    content: "";
    width: 24px;
    height: 56px;
    position: absolute;
    top: -32px;
  }

  .arm-left:before {
    border-radius: 50px 50px 0px 120px / 50px 50px 0 110px;
    left: 0;
    background: linear-gradient(135deg, #e3e8eb, #d0d5d8);
  }

  .arm-right:before {
    border-radius: 50px 50px 120px 0 / 50px 50px 110px 0;
    right: 0;
    background: linear-gradient(135deg, #fbfdfa, #e8eaec);
  }

  .arm-left:after,
  .arm-right:after {
    content: "";
    width: 24px;
    height: 8px;
    position: absolute;
    top: -19px;
  }

  .arm-left:after {
    background-color: #6e91a4;
    left: 0;
  }

  .arm-right:after {
    right: 0;
    background-color: #b6d2e0;
  }

  .leg {
    width: 24px;
    height: 32px;
    position: absolute;
    z-index: 2;
    bottom: 56px;
  }

  .leg-left {
    left: 61px;
    background: linear-gradient(135deg, #e3e8eb, #d0d5d8);
    transform: rotate(20deg);
  }

  .leg-right {
    right: 58px;
    background: linear-gradient(135deg, #fbfdfa, #e8eaec);
    transform: rotate(-20deg);
  }

  .leg-left:before,
  .leg-right:before {
    content: "";
    width: 40px;
    height: 20px;
    position: absolute;
    bottom: -21px;
  }

  .leg-left:before {
    left: -16px;
    background: linear-gradient(135deg, #e3e8eb, #d0d5d8);
    border-radius: 30px 0 0 0;
    border-bottom: 8px solid #6d96ac;
  }

  .leg-right:before {
    right: -16px;
    background: linear-gradient(135deg, #fbfdfa, #e8eaec);
    border-radius: 0 30px 0 0;
    border-bottom: 8px solid #b0cfe4;
  }

  /* ===== NEON GLOW EFFECTS ===== */
  .neon-text {
    text-shadow: 0 0 10px rgba(255,107,255,0.5),
                 0 0 20px rgba(255,107,255,0.3),
                 0 0 40px rgba(255,107,255,0.1);
  }

  .neon-box {
    box-shadow: 0 0 20px rgba(0,212,255,0.2),
                inset 0 0 20px rgba(0,212,255,0.05);
    border: 1px solid rgba(0,212,255,0.1);
    border-radius: 15px;
    padding: 20px;
    background: rgba(10,10,26,0.8);
    backdrop-filter: blur(10px);
  }

  .neon-border {
    border: 2px solid transparent;
    border-image: linear-gradient(45deg, #00FF88, #00D4FF, #FF6BFF, #00FF88);
    border-image-slice: 1;
    animation: borderGlow 3s linear infinite;
  }

  @keyframes borderGlow {
    0% { border-image: linear-gradient(45deg, #00FF88, #00D4FF, #FF6BFF, #00FF88); }
    50% { border-image: linear-gradient(225deg, #00FF88, #00D4FF, #FF6BFF, #00FF88); }
    100% { border-image: linear-gradient(45deg, #00FF88, #00D4FF, #FF6BFF, #00FF88); }
  }

  /* ===== CUSTOM SCROLL ===== */
  ::-webkit-scrollbar {
    width: 8px;
  }

  ::-webkit-scrollbar-track {
    background: #0a0a1a;
  }

  ::-webkit-scrollbar-thumb {
    background: linear-gradient(135deg, #00FF88, #00D4FF);
    border-radius: 4px;
  }

  ::-webkit-scrollbar-thumb:hover {
    background: linear-gradient(135deg, #00D4FF, #00FF88);
  }

  /* ===== RESPONSIVE ===== */
  @media (max-width: 768px) {
    .astronaut-container {
      right: 20px;
      bottom: 20px;
      transform: scale(0.6);
    }
    .star-position6, .star-position7 { display: none; }
  }
</style>

<!-- ===== SPACE BACKGROUND ===== -->
<div class="space-background"></div>
<div class="stars-layer" id="starsLayer"></div>

<!-- ===== FALLING STARS ===== -->
<div class="box-of-star1">
  <div class="star star-position1"></div>
  <div class="star star-position2"></div>
  <div class="star star-position3"></div>
  <div class="star star-position4"></div>
  <div class="star star-position5"></div>
  <div class="star star-position6"></div>
  <div class="star star-position7"></div>
</div>
<div class="box-of-star2">
  <div class="star star-position1"></div>
  <div class="star star-position2"></div>
  <div class="star star-position3"></div>
  <div class="star star-position4"></div>
  <div class="star star-position5"></div>
  <div class="star star-position6"></div>
  <div class="star star-position7"></div>
</div>
<div class="box-of-star3">
  <div class="star star-position1"></div>
  <div class="star star-position2"></div>
  <div class="star star-position3"></div>
  <div class="star star-position4"></div>
  <div class="star star-position5"></div>
  <div class="star star-position6"></div>
  <div class="star star-position7"></div>
</div>
<div class="box-of-star4">
  <div class="star star-position1"></div>
  <div class="star star-position2"></div>
  <div class="star star-position3"></div>
  <div class="star star-position4"></div>
  <div class="star star-position5"></div>
  <div class="star star-position6"></div>
  <div class="star star-position7"></div>
</div>

<!-- ===== ASTRONAUT ===== -->
<div class="astronaut-container">
  <div data-js="astro" class="astronaut">
    <div class="head"></div>
    <div class="arm arm-left"></div>
    <div class="arm arm-right"></div>
    <div class="body">
      <div class="panel"></div>
    </div>
    <div class="leg leg-left"></div>
    <div class="leg leg-right"></div>
    <div class="schoolbag"></div>
  </div>
</div>

<!-- ===== MAIN CONTENT ===== -->
<div style="position: relative; z-index: 5; padding: 20px; max-width: 1200px; margin: 0 auto;">

  <!-- ANIMAÇÃO DE DIGITAÇÃO NEON -->
  <p align="center" style="margin-top: 40px;">
    <img src="https://readme-typing-svg.herokuapp.com/?font=Orbitron&weight=900&size=30&duration=3000&pause=1000&color=00FF88&center=true&vCenter=true&width=1000&lines=Monique+Navarro;Full+Stack+Developer+%F0%9F%9A%80;Green+Tech+Enthusiast+%F0%9F%8C%B1;OT%2FIT+Integration+Specialist;Data+%26+Software+Engineer;Python+%7C+Node.js+%7C+Vue.js;IoT+%7C+MQTT+%7C+Modbus;ESG+%7C+Sustainability+%7C+Innovation;Welcome+to+my+tech+universe!+%F0%9F%8C%8C" alt="Typing SVG" />
  </p>

  <!-- BANNER NEON -->
  <p align="center">
    <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00FF88,100:00D4FF&height=140&section=header&text=Full%20Stack%20%7C%20Green%20Tech%20%F0%9F%9A%80&fontSize=26&fontAlignY=35&animation=twinkling&fontColor=FFFFFF" />
  </p>

  <p align="center" style="color: #00FF88; font-size: 18px; text-shadow: 0 0 20px rgba(0,255,136,0.3);">
    <i>✨ Bridging IT, OT, and ESG for a sustainable future ✨</i>
  </p>

  <br>

  <!-- BADGES NEON -->
  <p align="center">
    <a href="#"><img src="https://img.shields.io/badge/Full_Stack_Developer-00FF88?style=for-the-badge&logo=code&logoColor=white&labelColor=0A0A1A&color=00FF88" /></a>
    <a href="#"><img src="https://img.shields.io/badge/Green_Tech-00D4FF?style=for-the-badge&logo=leaf&logoColor=white&labelColor=0A0A1A&color=00D4FF" /></a>
    <a href="#"><img src="https://img.shields.io/badge/OT%2FIT_Integration-FF6BFF?style=for-the-badge&logo=industry&logoColor=white&labelColor=0A0A1A&color=FF6BFF" /></a>
    <a href="#"><img src="https://img.shields.io/badge/Data_Engineering-FFB800?style=for-the-badge&logo=data&logoColor=white&labelColor=0A0A1A&color=FFB800" /></a>
  </p>

  <!-- SOCIAL LINKS NEON -->
  <p align="center">
    <a href="https://www.linkedin.com/in/monique-navarro-eng/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0A0A1A&color=00FF88" /></a>
    <a href="https://github.com/Nikifit7"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white&labelColor=0A0A1A&color=00D4FF" /></a>
    <a href="https://codepen.io/nikifit7"><img src="https://img.shields.io/badge/CodePen-000000?style=for-the-badge&logo=codepen&logoColor=white&labelColor=0A0A1A&color=FFB800" /></a>
    <a href="mailto:esg.tech10@email.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0A0A1A&color=FF6B6B" /></a>
    <a href="#"><img src="https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=portfolio&logoColor=white&labelColor=0A0A1A&color=00FF88" /></a>
  </p>

  <br>

  <!-- DIVISÓRIA NEON -->
  <p align="center">
    <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" style="filter: hue-rotate(120deg) brightness(1.5);" />
  </p>

  <!-- ===== ABOUT ME ===== -->
  <div class="neon-box" style="margin: 30px 0; padding: 30px;">
    <h2 align="center" style="color: #00FF88; text-shadow: 0 0 30px rgba(0,255,136,0.3);">
      <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="28px" height="28px" style="filter: hue-rotate(120deg);"> About Me
    </h2>

    <div align="center">
      <img align="right" width="280" src="https://media.giphy.com/media/L1R1tvI9svkIWwp45Y/giphy.gif" style="border-radius: 20px; box-shadow: 0 0 40px rgba(0,255,136,0.3), 0 0 80px rgba(0,212,255,0.2);" />
    </div>

    <div style="color: #e0e0e0; font-size: 16px; line-height: 1.8;">
      <p>🚀 <strong style="color: #00FF88;">Monique Navarro</strong> — I live between the <strong style="color: #00D4FF;">IT/OT</strong> world and <strong style="color: #FF6BFF;">ESG</strong>, bridging data, software engineering, and sustainability.</p>
      
      <p>💡 <strong style="color: #00FF88;">Full Stack Developer</strong> passionate about code, sustainability, and process optimization.</p>
      
      <p>🌱 <strong style="color: #00D4FF;">Background:</strong></p>
      <ul style="color: #aaa; list-style: none; padding-left: 20px;">
        <li>🌿 Environmental Manager</li>
        <li>💻 Software Engineering Student</li>
        <li>🎨 Postgraduate in Full Stack Web Development</li>
        <li>🧠 Postgraduate in UI/UX Design & Neuroscience</li>
        <li>🏭 Industrial experience with Lean Manufacturing, TPM, Kanban & 5S</li>
      </ul>
      
      <p>🎯 <strong style="color: #FFB800;">What drives me:</strong></p>
      <ul style="color: #aaa; list-style: none; padding-left: 20px;">
        <li>🔧 Building systems that optimize industrial processes</li>
        <li>🌍 Applying technology for sustainability and ESG</li>
        <li>📊 Data-driven solutions with Python & Pandas</li>
        <li>🤖 IoT, MQTT, and Modbus for industrial automation</li>
        <li>💚 Clean code and innovative tech for a better world</li>
      </ul>
    </div>
  </div>

  <br>

  <!-- ===== TECH STACK ===== -->
  <div class="neon-box" style="margin: 30px 0; padding: 30px;">
    <h2 align="center" style="color: #00D4FF; text-shadow: 0 0 30px rgba(0,212,255,0.3);">
      <img src="https://media.giphy.com/media/WUlplcMpOCEmTGBtBW/giphy.gif" width="30px" style="filter: hue-rotate(120deg);"> Tech Stack
    </h2>

    <h3 style="color: #00FF88; text-align: center; font-size: 20px;">💻 Full Stack Development</h3>
    <p align="center">
      <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white&labelColor=0A0A1A&color=3776AB" />
      <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white&labelColor=0A0A1A&color=339933" />
      <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white&labelColor=0A0A1A&color=4FC08D" />
      <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=white&labelColor=0A0A1A&color=61DAFB" />
      <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white&labelColor=0A0A1A&color=00FF88" />
      <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white&labelColor=0A0A1A&color=3178C6" />
      <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white&labelColor=0A0A1A&color=F7DF1E" />
      <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white&labelColor=0A0A1A&color=777BB4" />
    </p>

    <h3 style="color: #FFB800; text-align: center; font-size: 20px; margin-top: 20px;">📊 Data & Analytics</h3>
    <p align="center">
      <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white&labelColor=0A0A1A&color=150458" />
      <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white&labelColor=0A0A1A&color=013243" />
      <img src="https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white&labelColor=0A0A1A&color=F9AB00" />
      <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white&labelColor=0A0A1A&color=F37626" />
      <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white&labelColor=0A0A1A&color=4479A1" />
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white&labelColor=0A0A1A&color=4169E1" />
    </p>

    <h3 style="color: #FF6BFF; text-align: center; font-size: 20px; margin-top: 20px;">🤖 IoT & Industrial</h3>
    <p align="center">
      <img src="https://img.shields.io/badge/IoT-FF6B6B?style=for-the-badge&logo=internet-of-things&logoColor=white&labelColor=0A0A1A&color=FF6B6B" />
      <img src="https://img.shields.io/badge/MQTT-660066?style=for-the-badge&logo=mqtt&logoColor=white&labelColor=0A0A1A&color=660066" />
      <img src="https://img.shields.io/badge/Modbus-0099CC?style=for-the-badge&logo=modbus&logoColor=white&labelColor=0A0A1A&color=0099CC" />
      <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white&labelColor=0A0A1A&color=2496ED" />
      <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=white&labelColor=0A0A1A&color=FCC624" />
      <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white&labelColor=0A0A1A&color=F05032" />
    </p>

    <h3 style="color: #00E676; text-align: center; font-size: 20px; margin-top: 20px;">🎨 UI/UX & Design</h3>
    <p align="center">
      <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white&labelColor=0A0A1A&color=F24E1E" />
      <img src="https://img.shields.io/badge/Adobe_XD-FF61F6?style=for-the-badge&logo=adobe-xd&logoColor=white&labelColor=0A0A1A&color=FF61F6" />
      <img src="https://img.shields.io/badge/GSAP-88CE02?style=for-the-badge&logo=greensock&logoColor=white&labelColor=0A0A1A&color=88CE02" />
      <img src="https://img.shields.io/badge/Framer_Motion-0055FF?style=for-the-badge&logo=framer&logoColor=white&labelColor=0A0A1A&color=0055FF" />
      <img src="https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white&labelColor=0A0A1A&color=00FF88" />
    </p>

    <h3 style="color: #00D4FF; text-align: center; font-size: 20px; margin-top: 20px;">🏭 Industrial Knowledge</h3>
    <p align="center">
      <img src="https://img.shields.io/badge/Lean_Manufacturing-00FF88?style=flat-square&logo=industry&logoColor=white&labelColor=0A0A1A&color=00FF88" />
      <img src="https://img.shields.io/badge/TPM-00D4FF?style=flat-square&logo=gear&logoColor=white&labelColor=0A0A1A&color=00D4FF" />
      <img src="https://img.shields.io/badge/Kanban-FF6BFF?style=flat-square&logo=trello&logoColor=white&labelColor=0A0A1A&color=FF6BFF" />
      <img src="https://img.shields.io/badge/5S-FFB800?style=flat-square&logo=check&logoColor=white&labelColor=0A0A1A&color=FFB800" />
      <img src="https://img.shields.io/badge/SAP-0FAAFF?style=flat-square&logo=sap&logoColor=white&labelColor=0A0A1A&color=0FAAFF" />
      <img src="https://img.shields.io/badge/ISO_9001-00FF88?style=flat-square&logo=iso&logoColor=white&labelColor=0A0A1A&color=00FF88" />
      <img src="https://img.shields.io/badge/ISO_14001-00D4FF?style=flat-square&logo=iso&logoColor=white&labelColor=0A0A1A&color=00D4FF" />
      <img src="https://img.shields.io/badge/ISO_50001-FFB800?style=flat-square&logo=iso&logoColor=white&labelColor=0A0A1A&color=FFB800" />
    </p>
  </div>

  <br>

  <!-- ===== WHAT I'M LOOKING FOR ===== -->
  <div class="neon-box" style="margin: 30px 0; padding: 30px;">
    <h2 align="center" style="color: #FFB800; text-shadow: 0 0 30px rgba(255,184,0,0.3);">
      <img src="https://media.giphy.com/media/ZVik7pBtu9dNS/giphy.gif" width="30px" style="filter: hue-rotate(120deg);"> What I'm Looking For
    </h2>
    <p align="center" style="color: #e0e0e0; font-size: 16px;">
      Opportunities to grow as a <strong style="color: #00FF88;">Full Stack Developer</strong> while applying technology to solve real-world industrial and sustainability challenges.
    </p>
    <br>
    <p align="center">
      <img src="https://img.shields.io/badge/Software_Engineering-00FF88?style=for-the-badge&logo=code&logoColor=white&labelColor=0A0A1A&color=00FF88" />
      <img src="https://img.shields.io/badge/Data_Engineering-00D4FF?style=for-the-badge&logo=data&logoColor=white&labelColor=0A0A1A&color=00D4FF" />
      <img src="https://img.shields.io/badge/Process_Automation-FF6BFF?style=for-the-badge&logo=automation&logoColor=white&labelColor=0A0A1A&color=FF6BFF" />
      <img src="https://img.shields.io/badge/Industrial_Digitalization-FFB800?style=for-the-badge&logo=industry&logoColor=white&labelColor=0A0A1A&color=FFB800" />
      <img src="https://img.shields.io/badge/Sustainability_Tech-00FF88?style=for-the-badge&logo=leaf&logoColor=white&labelColor=0A0A1A&color=00FF88" />
      <img src="https://img.shields.io/badge/IoT_Integration-FF6B6B?style=for-the-badge&logo=internet-of-things&logoColor=white&labelColor=0A0A1A&color=FF6B6B" />
    </p>
  </div>

  <br>

  <!-- ===== LANGUAGES ===== -->
  <div class="neon-box" style="margin: 30px 0; padding: 30px;">
    <h2 align="center" style="color: #00D4FF; text-shadow: 0 0 30px rgba(0,212,255,0.3);">🌍 Languages</h2>
    <p align="center">
      <img src="https://img.shields.io/badge/Portuguese-Native-00FF88?style=for-the-badge&logo=brazil&logoColor=white&labelColor=0A0A1A&color=00FF88" />
      <img src="https://img.shields.io/badge/English-Professional-00D4FF?style=for-the-badge&logo=united-kingdom&logoColor=white&labelColor=0A0A1A&color=00D4FF" />
      <img src="https://img.shields.io/badge/Spanish-Intermediate-FFB800?style=for-the-badge&logo=spain&logoColor=white&labelColor=0A0A1A&color=FFB800" />
      <img src="https://img.shields.io/badge/German-Intermediate-FF6BFF?style=for-the-badge&logo=germany&logoColor=white&labelColor=0A0A1A&color=FF6BFF" />
    </p>
  </div>

  <br>

  <!-- ===== GITHUB STATS ===== -->
  <div class="neon-box" style="margin: 30px 0; padding: 30px;">
    <h2 align="center" style="color: #00FF88; text-shadow: 0 0 30px rgba(0,255,136,0.3);">📊 GitHub Stats</h2>
    <p align="center">
      <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Nikifit7&show_icons=true&theme=radical&include_all_commits=true&count_private=true&bg_color=0A0A1A&title_color=00FF88&text_color=00D4FF&icon_color=FFB800" />
      <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Nikifit7&layout=compact&langs_count=7&theme=radical&bg_color=0A0A1A&title_color=00FF88&text_color=00D4FF&icon_color=FFB800" />
    </p>
    <p align="center">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=Nikifit7&theme=radical&background=0A0A1A&ring=00FF88&fire=00D4FF&currStreakLabel=FFB800" />
    </p>
  </div>

  <br>

  <!-- ===== PAC-MAN ===== -->
  <p align="center">
    <img src="https://github.com/platane/snk/raw/output/github-contribution-grid-snake-dark.svg" width="100%" style="filter: hue-rotate(120deg);">
  </p>

  <p align="center" style="color: #00FF88; text-shadow: 0 0 20px rgba(0,255,136,0.3);">
    <i>🌱 Code. Sustainability. Innovation. Repeat. 🚀</i>
  </p>

  <br>

  <!-- ===== FOOTER ===== -->
  <p align="center">
    <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00FF88,100:00D4FF&height=100&section=footer" />
  </p>

  <p align="center" style="color: #888; font-size: 14px;">
    <i>✨ "The best way to predict the future is to create it." — Peter Drucker</i>
  </p>

  <p align="center" style="color: #555; font-size: 12px;">
    <i>🌱 © Monique Navarro 2026 — Full Stack | Green Tech | ESG Edition</i>
  </p>
</div>

<!-- ===== GSAP & SCRIPTS ===== -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>
<script>
  // Register GSAP plugins
  gsap.registerPlugin(ScrollTrigger);

  // Generate background stars
  function createStars() {
    const container = document.getElementById('starsLayer');
    for (let i = 0; i < 200; i++) {
      const star = document.createElement('div');
      star.className = 'star-bg';
      const size = Math.random() * 3 + 1;
      star.style.cssText = `
        width: ${size}px;
        height: ${size}px;
        top: ${Math.random() * 100}%;
        left: ${Math.random() * 100}%;
        --duration: ${Math.random() * 3 + 2}s;
        animation-delay: ${Math.random() * 3}s;
        opacity: ${Math.random() * 0.5 + 0.3};
      `;
      container.appendChild(star);
    }
  }
  createStars();

  // Animate badges with GSAP
  gsap.utils.toArray('img[src*="shields.io"]').forEach((badge, i) => {
    gsap.from(badge, {
      opacity: 0,
      scale: 0,
      rotation: 360,
      duration: 0.6,
      delay: i * 0.05,
      ease: 'back.out(1.7)',
      scrollTrigger: {
        trigger: badge,
        start: 'top bottom-=50',
        toggleActions: 'play none none reverse'
      }
    });
  });

  // Animate neon boxes
  gsap.utils.toArray('.neon-box').forEach((box, i) => {
    gsap.from(box, {
      opacity: 0,
      y: 50,
      duration: 1,
      delay: i * 0.2,
      scrollTrigger: {
        trigger: box,
        start: 'top bottom-=100',
        toggleActions: 'play none none reverse'
      }
    });
  });

  // Animate titles
  gsap.utils.toArray('h2, h3').forEach((title) => {
    gsap.from(title, {
      opacity: 0,
      y: -30,
      duration: 0.8,
      ease: 'bounce.out',
      scrollTrigger: {
        trigger: title,
        start: 'top bottom-=80',
        toggleActions: 'play none none reverse'
      }
    });
  });

  // Floating particles effect
  const colors = ['#00FF88', '#00D4FF', '#FF6BFF', '#FFB800'];
  for (let i = 0; i < 15; i++) {
    const particle = document.createElement('div');
    particle.style.cssText = `
      position: fixed;
      width: ${Math.random() * 4 + 2}px;
      height: ${Math.random() * 4 + 2}px;
      background: ${colors[i % colors.length]};
      border-radius: 50%;
      pointer-events: none;
      z-index: 0;
      box-shadow: 0 0 20px ${colors[i % colors.length]};
      opacity: ${Math.random() * 0.3 + 0.1};
      left: ${Math.random() * 100}vw;
      top: ${Math.random() * 100}vh;
    `;
    document.body.appendChild(particle);
    
    gsap.to(particle, {
      x: () => gsap.utils.random(-200, 200),
      y: () => gsap.utils.random(-200, 200),
      scale: () => gsap.utils.random(0.5, 2),
      duration: () => gsap.utils.random(10, 20),
      repeat: -1,
      yoyo: true,
      ease: 'sine.inOut',
      delay: i * 0.5
    });
  }

  console.log('🚀 Full Stack | Green Tech Profile loaded!');
  console.log('🌱 Made with ❤️ by Monique Navarro');
</script>
