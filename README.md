Here is your GitHub-ready README in English, packed with colorful icons, GSAP animations, and a clean industrial dashboard vibe — no unverified numbers, just a stylish and humble presentation of your skills.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Monique Navarro | ESG Industrial Data & Industry 4.0</title>
    <!-- Google Fonts: modern & technical -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">
    <!-- Font Awesome 6 (free icons) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- GSAP core & ScrollTrigger -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #f7f2ea 0%, #ede4d8 100%);
            font-family: 'Inter', sans-serif;
            color: #1f2a2e;
            overflow-x: hidden;
            scroll-behavior: smooth;
            position: relative;
        }

        /* handmade texture overlay */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 400 300" opacity="0.05"><filter id="noise"><feTurbulence type="fractalNoise" baseFrequency="0.7" numOctaves="3" stitchTiles="stitch"/></filter><rect width="100%" height="100%" filter="url(%23noise)"/></svg>');
            pointer-events: none;
            z-index: 0;
        }

        /* rotating gears background (colorful, craft vibes) */
        .gear-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
            opacity: 0.35;
        }

        .gear {
            position: absolute;
            font-size: 6.5rem;
            filter: drop-shadow(2px 4px 8px rgba(0,0,0,0.1));
            animation: rotateGear linear infinite;
        }

        .gear:nth-child(1) { color: #e67e22; top: 2%; left: -2%; animation-duration: 24s; }
        .gear:nth-child(2) { color: #2c7da0; bottom: 5%; right: -3%; animation-duration: 32s; animation-direction: reverse; }
        .gear:nth-child(3) { color: #e9b35f; top: 45%; left: 88%; font-size: 5rem; animation-duration: 20s; }
        .gear:nth-child(4) { color: #bc6c25; bottom: 25%; left: 3%; font-size: 5rem; animation-duration: 28s; animation-direction: reverse; }
        .gear:nth-child(5) { color: #d9a13b; top: 75%; left: 12%; font-size: 4.8rem; animation-duration: 22s; }
        .gear:nth-child(6) { color: #8b5a2b; top: 15%; left: 45%; font-size: 4rem; animation-duration: 36s; opacity: 0.5; }

        @keyframes rotateGear {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .container {
            position: relative;
            z-index: 2;
            max-width: 1280px;
            margin: 0 auto;
            padding: 2rem 1.5rem 3rem;
        }

        /* card with warm, artisanal feel */
        .hero {
            background: #fffaf2;
            border-radius: 3rem 2rem 3rem 2rem;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 10px 10px 0 #d9c2a7;
            border: 1px solid #f3d9b5;
            transition: all 0.2s;
        }

        .badge-line {
            display: flex;
            flex-wrap: wrap;
            gap: 0.75rem;
            margin: 1rem 0;
            justify-content: center;
        }

        .badge {
            background: #fef3e4;
            padding: 0.4rem 1.2rem;
            border-radius: 60px;
            font-size: 0.8rem;
            font-weight: 600;
            color: #7b4a2e;
            border-left: 4px solid #f39c12;
            font-family: 'Fira Code', monospace;
            box-shadow: 1px 2px 3px rgba(0,0,0,0.05);
        }

        h1 {
            font-size: 3.8rem;
            font-weight: 800;
            color: #3b2a1f;
            letter-spacing: -0.02em;
            text-shadow: 3px 3px 0 #f2d9b0;
        }

        .sub {
            font-size: 1.15rem;
            color: #5f4c38;
            max-width: 750px;
            margin: 1rem auto;
            background: #fff3e6;
            display: inline-block;
            padding: 0.5rem 1.4rem;
            border-radius: 60px;
            font-weight: 500;
        }

        .glass-card {
            background: #fef9f0;
            border-radius: 2rem;
            padding: 1.8rem;
            border: 1px solid #f7d9ae;
            box-shadow: 8px 8px 0 #ddc6a2;
            transition: transform 0.2s ease, box-shadow 0.2s;
        }

        .glass-card:hover {
            transform: translate(-3px, -3px);
            box-shadow: 12px 12px 0 #c7a878;
        }

        .icon-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.9rem;
            justify-content: center;
            margin: 1.5rem 0;
        }

        .tech-icon {
            background: #fff3e0;
            border-radius: 60px;
            padding: 0.5rem 1.2rem;
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            font-size: 0.85rem;
            font-weight: 600;
            font-family: 'Fira Code', monospace;
            border: 1px solid #f3cd81;
            color: #7c5227;
            transition: all 0.2s;
            box-shadow: 1px 2px 3px rgba(0,0,0,0.05);
        }

        .tech-icon i, .tech-icon .fab, .tech-icon .fas {
            font-size: 1.2rem;
            color: #e67e22;
        }

        .section-title {
            font-size: 1.8rem;
            margin-bottom: 1.2rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 0.8rem;
            border-left: 6px solid #f97316;
            padding-left: 1rem;
            color: #4a2a16;
        }

        .grid-2col {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }

        .timeline-text {
            line-height: 1.5;
            color: #3f2e1f;
        }

        hr {
            margin: 1.8rem 0;
            border-color: #f7cf9f;
        }

        footer {
            text-align: center;
            margin-top: 3rem;
            font-size: 0.8rem;
            color: #9b7e62;
            background: #f9ecd9;
            padding: 1rem;
            border-radius: 3rem;
        }

        .btn-linkedin {
            background: #0077b5;
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 60px;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: 0.2s;
            color: white;
            text-decoration: none;
            box-shadow: 2px 2px 0 #004b6e;
        }

        .btn-github {
            background: #4c2f1d;
            border: 1px solid #e6b46b;
            box-shadow: 2px 2px 0 #2c1a0e;
        }

        .btn-linkedin:hover {
            transform: translateY(-2px);
            filter: brightness(1.03);
        }

        .card-note {
            background: #fff7ef;
            border-left: 8px solid #f59e0b;
        }

        @media (max-width: 700px) {
            h1 { font-size: 2.4rem; }
            .hero { padding: 1.5rem; }
        }
    </style>
</head>
<body>

<div class="gear-bg">
    <div class="gear"><i class="fas fa-cog"></i></div>
    <div class="gear"><i class="fas fa-gear"></i></div>
    <div class="gear"><i class="fas fa-cog"></i></div>
    <div class="gear"><i class="fas fa-gear"></i></div>
    <div class="gear"><i class="fas fa-cog"></i></div>
    <div class="gear"><i class="fas fa-gear"></i></div>
</div>

<div class="container">
    <!-- Hero section -->
    <div class="hero" id="heroAnim">
        <div align="center">
            <h1>🌱 Monique Navarro</h1>
            <div class="badge-line">
                <span class="badge"><i class="fas fa-chalkboard-user"></i> Environmental Manager</span>
                <span class="badge"><i class="fas fa-laptop-code"></i> Pós Web Dev Full Stack</span>
                <span class="badge"><i class="fas fa-chart-line"></i> ESG Industrial Data</span>
                <span class="badge"><i class="fas fa-industry"></i> Waste Hunter 4.0</span>
            </div>
            <p class="sub">
                🔧 Bridging shopfloor efficiency & data — turning industrial data into sustainable decisions.<br>
                OT-IT Integration · Modbus · MQTT · OPC UA · Python · SQL · Node-RED
            </p>
            <div style="margin: 1rem 0;">
                <a href="https://www.linkedin.com/in/monique-navarro-eng/" target="_blank" class="btn-linkedin" style="margin-right: 1rem;"><i class="fab fa-linkedin"></i> LinkedIn</a>
                <a href="https://github.com/monique-navarro-eng" target="_blank" class="btn-linkedin btn-github"><i class="fab fa-github"></i> GitHub</a>
            </div>
        </div>
    </div>

    <!-- Humble & smart statement - no AI mention, pure craft -->
    <div class="glass-card card-note" style="text-align: center;" id="cardFrase">
        <p style="font-size: 1.2rem; font-weight: 500;">📢 “Waste reduction is survival. I merge ISO 14001, 50001, field sensors, and real code. Ex-Natura, rural background, now based in Germany — connecting hardware, protocols, and dashboards.”</p>
        <div style="margin-top: 0.8rem;"><i class="fas fa-wrench"></i> ISO 9001 · 14001 · 50001 · SAP basic · TPM · Circular Economy</div>
    </div>

    <!-- Full tech stack with GSAP explicitly included -->
    <div class="glass-card" id="stackCard">
        <div class="section-title">
            <i class="fas fa-microchip" style="color:#e67e22;"></i>
            <span>⚙️ Industrial Stack · Data & Integration</span>
        </div>
        <div class="icon-stack">
            <span class="tech-icon"><i class="fab fa-python"></i> Python</span>
            <span class="tech-icon"><i class="fab fa-html5"></i> HTML5</span>
            <span class="tech-icon"><i class="fab fa-css3-alt"></i> CSS3</span>
            <span class="tech-icon"><i class="fab fa-js"></i> JavaScript</span>
            <span class="tech-icon"><i class="fab fa-node-js"></i> Node.js</span>
            <span class="tech-icon"><i class="fas fa-database"></i> SQL / Big Data</span>
            <span class="tech-icon"><i class="fas fa-chalkboard"></i> Google Sheets / Colab</span>
            <span class="tech-icon"><i class="fas fa-code-branch"></i> Node-RED</span>
            <span class="tech-icon"><i class="fas fa-exchange-alt"></i> MQTT</span>
            <span class="tech-icon"><i class="fas fa-plug"></i> Modbus</span>
            <span class="tech-icon"><i class="fas fa-shield-alt"></i> OPC UA</span>
            <span class="tech-icon"><i class="fas fa-palette"></i> UI/UX</span>
            <span class="tech-icon"><i class="fas fa-chart-line"></i> GSAP</span>
        </div>
        <div class="icon-stack">
            <span class="tech-icon"><i class="fas fa-certificate"></i> ISO 9001</span>
            <span class="tech-icon"><i class="fas fa-leaf"></i> ISO 14001</span>
            <span class="tech-icon"><i class="fas fa-bolt"></i> ISO 50001</span>
            <span class="tech-icon"><i class="fab fa-sap"></i> SAP (basic)</span>
            <span class="tech-icon"><i class="fas fa-chart-simple"></i> Power BI</span>
            <span class="tech-icon"><i class="fas fa-charging-station"></i> GHG / ESG</span>
        </div>
        <div class="timeline-text" style="margin-top: 1rem; font-size: 0.9rem; background:#fef2e4; padding: 0.6rem; border-radius: 2rem;">
            <i class="fas fa-check-circle" style="color:#f97316;"></i> Modbus TCP/RTU · MQTT broker · OPC UA data pipelines · Real-time energy & OEE tracking · Custom dashboards for waste hunting.
        </div>
    </div>

    <!-- Highlight projects - no fake numbers, just description -->
    <div class="grid-2col">
        <div class="glass-card" id="projetoCard1">
            <i class="fas fa-charging-station" style="font-size: 2rem; color:#e67e22;"></i>
            <h3 style="margin: 0.7rem 0;">🔌 Real-time Energy Monitoring</h3>
            <p>Node-RED + MQTT collecting live data from Modbus inverters and PLCs. Python processing for anomaly detection and automated ISO 50001 reports. Actionable insights for shopfloor energy efficiency.</p>
            <div><i class="fas fa-chart-line"></i> <strong>Stack:</strong> Python · SQL · Node-RED · GSAP dashboard</div>
        </div>

        <div class="glass-card" id="projetoCard2">
            <i class="fas fa-tint" style="font-size: 2rem; color:#e67e22;"></i>
            <h3 style="margin: 0.7rem 0;">💧 Water & Waste Circularity</h3>
            <p>OPC UA sensors + SQL + Google Sheets pipeline. Interactive dashboard tracking reuse indicators, aligned with ISO 14001. Supporting data-driven decisions for reducing freshwater consumption.</p>
            <div><i class="fas fa-database"></i> <strong>Tools:</strong> Python · SQL · Google Data Studio · GSAP</div>
        </div>
    </div>

    <!-- Journey & ESG focus - no hard numbers, just experience -->
    <div class="glass-card" id="jornadaCard">
        <div class="section-title">
            <i class="fas fa-road"></i>
            <span>🧭 Journey: from environmental field to industrial data fusion</span>
        </div>
        <div style="display: flex; flex-wrap: wrap; gap: 1.8rem; justify-content: space-between;">
            <div style="flex:1; min-width: 180px;">
                <p><i class="fas fa-check-circle" style="color:#f97316;"></i> <strong>Ex-Natura</strong> – environmental KPIs & TPM implementation</p>
                <p><i class="fas fa-check-circle" style="color:#f97316;"></i> <strong>7 years rural management</strong> – resource efficiency & waste prevention</p>
                <p><i class="fas fa-check-circle" style="color:#f97316;"></i> <strong>Environmental Manager ESG</strong> – ISO 14001 & 50001 internal audits</p>
            </div>
            <div style="flex:1; min-width: 180px;">
                <p><i class="fas fa-microchip"></i> <strong>Full Stack + Industrial Dev</strong> – custom dashboards, JS, GSAP</p>
                <p><i class="fas fa-plug"></i> <strong>IIoT Integrator</strong> – OPC UA, Modbus, MQTT, Node-RED workflows</p>
                <p><i class="fas fa-search"></i> <strong>Waste hunting</strong> – energy leaks, reactive power, thermal losses, water overuse</p>
            </div>
        </div>
        <hr>
        <div align="center" style="gap: 1rem; display: flex; flex-wrap: wrap; justify-content: center;">
            <div><span class="valor-destaque" style="font-size:1.3rem;">📉 Proven waste reduction</span> <span style="color:#5b3e25;">through data & field validation</span></div>
            <div><span class="valor-destaque" style="font-size:1.3rem;">📈 Real-time visibility</span> <span style="color:#5b3e25;">for shopfloor decisions</span></div>
        </div>
    </div>

    <!-- Industrial protocols & standards -->
    <div class="glass-card" id="protocolos">
        <div class="section-title"><i class="fas fa-network-wired"></i> <span>Protocols & Standards that connect people and machines</span></div>
        <div style="display: flex; flex-wrap: wrap; gap: 1rem; justify-content: center;">
            <div class="tech-icon"><i class="fas fa-exchange-alt"></i> Modbus TCP/RTU</div>
            <div class="tech-icon"><i class="fas fa-comment-dots"></i> MQTT</div>
            <div class="tech-icon"><i class="fas fa-shield-alt"></i> OPC UA</div>
            <div class="tech-icon"><i class="fas fa-chart-line"></i> OEE / Overall Equipment Effectiveness</div>
            <div class="tech-icon"><i class="fas fa-leaf"></i> GHG Protocol</div>
            <div class="tech-icon"><i class="fas fa-tachometer-alt"></i> SCADA & Historians</div>
        </div>
        <p class="timeline-text" style="margin-top: 1rem; text-align: center; background:#fff2e4; padding: 0.7rem; border-radius: 1.5rem;">“Every bit from a PLC or sensor is an opportunity to cut cost and environmental impact. I build that bridge.”</p>
    </div>

    <!-- Location & languages -->
    <div class="glass-card" style="text-align: center;" id="localCard">
        <i class="fas fa-map-marker-alt" style="font-size: 2rem; color:#e67e22;"></i>
        <h3 style="margin: 0.5rem 0;">📍 Based in Germany · Industry 4.0 ready</h3>
        <p>Driving digital transformation in the German industrial sector with an environmental lens. Open for OT-IT integration, energy efficiency projects, and shopfloor dashboards.</p>
        <div style="margin-top: 1rem;">
            <span class="badge">🇩🇪 Deutsch B1 (improving)</span>
            <span class="badge">🇬🇧 English · technical & business</span>
            <span class="badge">🇵🇹 Portuguese native</span>
        </div>
        <div style="margin-top: 1rem;"><i class="fas fa-globe-europe"></i> Open to networking & real industrial collaborations</div>
    </div>

    <footer>
        <i class="fas fa-cogs"></i> Industrial data · Environmental ethics · Handcrafted code <br>
        Monique Navarro — every data point tells an efficiency story. <br>
        © 2026 · Waste hunting as a survival mindset.
    </footer>
</div>

<script>
    gsap.registerPlugin(ScrollTrigger);
    
    // gentle entrance animations
    const tlHero = gsap.timeline();
    tlHero.from("#heroAnim", { opacity: 0, y: -35, duration: 0.9, ease: "back.out(0.6)" })
          .from("#heroAnim .badge", { opacity: 0, scale: 0.9, stagger: 0.08, duration: 0.5 }, "-=0.4")
          .from("#heroAnim .sub", { opacity: 0, x: -20, duration: 0.6 }, "-=0.3")
          .from("#heroAnim .btn-linkedin", { opacity: 0, y: 15, stagger: 0.1, duration: 0.5 }, "-=0.2");
    
    gsap.from("#cardFrase", { opacity: 0, y: 20, duration: 0.7, scrollTrigger: { trigger: "#cardFrase", start: "top 88%" } });
    gsap.from("#stackCard", { opacity: 0, y: 30, duration: 0.8, scrollTrigger: { trigger: "#stackCard", start: "top 85%" } });
    gsap.from("#projetoCard1", { opacity: 0, x: -35, duration: 0.7, scrollTrigger: { trigger: "#projetoCard1", start: "top 85%" } });
    gsap.from("#projetoCard2", { opacity: 0, x: 35, duration: 0.7, scrollTrigger: { trigger: "#projetoCard2", start: "top 85%" } });
    gsap.from("#jornadaCard", { opacity: 0, y: 25, duration: 0.7, scrollTrigger: { trigger: "#jornadaCard", start: "top 85%" } });
    gsap.from("#protocolos", { opacity: 0, scale: 0.98, duration: 0.7, scrollTrigger: { trigger: "#protocolos", start: "top 85%" } });
    gsap.from("#localCard", { opacity: 0, y: 20, duration: 0.6, scrollTrigger: { trigger: "#localCard", start: "top 85%" } });
    
    // floating animation for gears - subtle and artisanal
    const gears = document.querySelectorAll('.gear');
    gears.forEach((gear, idx) => {
        gsap.to(gear, {
            y: "random(-7, 7)",
            duration: 3 + idx,
            repeat: -1,
            yoyo: true,
            ease: "sine.inOut",
            delay: idx * 0.25
        });
    });
    
    // hover effects on tech badges
    const techBadges = document.querySelectorAll('.tech-icon');
    techBadges.forEach(badge => {
        badge.addEventListener('mouseenter', () => {
            gsap.to(badge, { backgroundColor: "#fbe9c3", scale: 1.02, borderColor: "#f59e0b", duration: 0.2 });
        });
        badge.addEventListener('mouseleave', () => {
            gsap.to(badge, { backgroundColor: "#fff3e0", scale: 1, borderColor: "#f3cd81", duration: 0.2 });
        });
    });
    
    // tooltips for protocols (manual, no AI)
    const protoTips = document.querySelectorAll('#protocolos .tech-icon');
    protoTips.forEach(item => {
        let tooltipMsg = "";
        if (item.innerText.includes("Modbus")) tooltipMsg = "Direct communication with PLCs, drives, energy meters";
        else if (item.innerText.includes("MQTT")) tooltipMsg = "Lightweight telemetry for industrial IoT";
        else if (item.innerText.includes("OPC UA")) tooltipMsg = "Secure interoperability standard for IIoT";
        else if (item.innerText.includes("ISO 50001")) tooltipMsg = "Energy management system — real results";
        else if (item.innerText.includes("OEE")) tooltipMsg = "Overall Equipment Effectiveness tracking";
        else tooltipMsg = "Industry protocol / standard applied to waste hunting";
        item.setAttribute("title", tooltipMsg);
    });
    
    // small console signature, humble and proud
    console.log("🌿 Monique Navarro · GitHub README · Industrial data + sustainability · handcrafted with GSAP");
</script>
</body>
</html>
```
