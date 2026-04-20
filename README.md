<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <title>Monique Navarro | Industrie 4.0 Ingenieurin</title>
    <!-- Google Fonts & Font Awesome -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- GSAP Core & Plugins -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/MotionPathPlugin.min.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #0A0F1E 0%, #0C1222 100%);
            font-family: 'Inter', sans-serif;
            color: #EFF3FC;
            line-height: 1.5;
            overflow-x: hidden;
        }

        /* Glow-Effekte und industrielle Texturen */
        .industrial-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 600" opacity="0.03"><path fill="none" stroke="%2344aaff" stroke-width="0.8" d="M0 300 L800 300 M400 0 L400 600 M100 100 L700 500 M700 100 L100 500"/><circle cx="200" cy="150" r="80" stroke="%2344aaff" stroke-width="0.5"/><circle cx="600" cy="450" r="120" stroke="%2344aaff" stroke-width="0.5"/></svg>');
            background-repeat: repeat;
            pointer-events: none;
            z-index: 0;
        }

        .container {
            max-width: 1300px;
            margin: 0 auto;
            padding: 2rem 2rem 4rem;
            position: relative;
            z-index: 2;
        }

        /* Header mit rotierendem Zahnrad */
        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            margin-bottom: 5rem;
            position: relative;
        }

        .gear-wrapper {
            width: 160px;
            height: 160px;
            margin-bottom: 1.5rem;
            filter: drop-shadow(0 0 15px rgba(0, 180, 255, 0.4));
        }

        .gear-wrapper img {
            width: 100%;
            animation: spinSlow 12s linear infinite;
        }

        @keyframes spinSlow {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        h1 {
            font-size: 3.8rem;
            font-weight: 800;
            background: linear-gradient(135deg, #FFFFFF, #7AC7FF);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: -0.02em;
            margin-bottom: 0.75rem;
        }

        .subtitle {
            font-size: 1.4rem;
            font-weight: 500;
            color: #9BB4D4;
            border-bottom: 2px solid #2C3E66;
            display: inline-block;
            padding-bottom: 0.5rem;
            margin-bottom: 1rem;
        }

        .mission {
            max-width: 700px;
            font-size: 1.1rem;
            color: #B8C9E8;
            background: rgba(16, 24, 40, 0.6);
            backdrop-filter: blur(4px);
            padding: 1rem 1.8rem;
            border-radius: 60px;
            border-left: 4px solid #3B82F6;
        }

        /* Sektionen allgemein */
        section {
            background: rgba(18, 25, 45, 0.6);
            backdrop-filter: blur(2px);
            border-radius: 2rem;
            padding: 2rem 2rem;
            margin-bottom: 3rem;
            border: 1px solid rgba(59, 130, 246, 0.25);
            transition: all 0.3s ease;
            box-shadow: 0 20px 35px -12px rgba(0,0,0,0.4);
        }

        .section-title {
            font-size: 1.8rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 1.8rem;
            border-left: 5px solid #3B82F6;
            padding-left: 1.2rem;
        }

        .section-title i {
            color: #3B82F6;
            font-size: 1.8rem;
        }

        .tech-grid, .badge-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
            margin: 1.5rem 0;
        }

        .tech-card {
            background: #0F172A;
            padding: 0.8rem 1.6rem;
            border-radius: 2rem;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            font-weight: 600;
            border: 1px solid #2D3A5E;
            transition: transform 0.2s, border-color 0.2s;
            box-shadow: 0 5px 12px rgba(0,0,0,0.2);
        }

        .tech-card i, .tech-card .fab {
            font-size: 1.8rem;
        }

        .tech-card:hover {
            transform: translateY(-5px);
            border-color: #3B82F6;
            background: #1E2A46;
        }

        /* Industrielle Protokolle speziell */
        .protocol-list {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
        }

        .protocol-item {
            background: linear-gradient(145deg, #111827, #0B0F1A);
            padding: 0.6rem 1.4rem;
            border-radius: 40px;
            font-family: monospace;
            font-weight: bold;
            color: #93C5FD;
            border: 1px solid #1E3A8A;
        }

        /* EdTech Hervorhebung */
        .edtech-highlight {
            background: linear-gradient(120deg, #0F172A, #111C36);
            border-left: 8px solid #F59E0B;
            padding: 1.2rem 1.8rem;
            border-radius: 1.5rem;
            margin-top: 1rem;
        }

        /* Projekte */
        .projects-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 1.8rem;
            margin-top: 1rem;
        }

        .project-card {
            flex: 1 1 280px;
            background: rgba(12, 20, 30, 0.8);
            border-radius: 1.5rem;
            padding: 1.5rem;
            transition: all 0.3s;
            border: 1px solid #2C3E66;
        }

        .project-card i {
            font-size: 2.2rem;
            color: #3B82F6;
            margin-bottom: 1rem;
        }

        .project-card h3 {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
        }

        .project-card p {
            color: #B9CAF0;
            font-size: 0.9rem;
        }

        /* Footer & Social */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0 1rem;
        }

        .social-icon {
            background: #1E293B;
            width: 55px;
            height: 55px;
            border-radius: 30px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            transition: all 0.2s;
            color: #CBD5E1;
            text-decoration: none;
        }

        .social-icon:hover {
            background: #3B82F6;
            color: white;
            transform: scale(1.1);
            box-shadow: 0 0 15px #3B82F6;
        }

        .footer-copyright {
            text-align: center;
            font-size: 0.8rem;
            color: #5B6D8C;
            border-top: 1px solid #1F2A44;
            padding-top: 2rem;
            margin-top: 2rem;
        }

        /* animierte Linie */
        .animated-line {
            height: 2px;
            background: linear-gradient(90deg, transparent, #3B82F6, #60A5FA, transparent);
            width: 0%;
            margin: 1rem auto;
        }

        @media (max-width: 768px) {
            h1 { font-size: 2.3rem; }
            .container { padding: 1rem; }
            .section-title { font-size: 1.5rem; }
        }
    </style>
</head>
<body>

<div class="industrial-bg"></div>

<div class="container">
    <!-- Hero Bereich -->
    <div class="hero" id="hero">
        <div class="gear-wrapper">
            <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNHJqbmV4ZzY0eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/l41lTjJp8yYyG2bkc/giphy.gif" alt="Rotating Gears" />
        </div>
        <h1 id="mainTitle">Monique Navarro</h1>
        <div class="subtitle" id="subHeadline">
            <i class="fas fa-microchip"></i> Industrial Transformation Engineer | Data Enthusiast | Frontend Explorer
        </div>
        <p class="mission" id="missionText">
            <i class="fas fa-bridge"></i> Die Brücke zwischen Shopfloor-Effizienz und modernen digitalen Erlebnissen schlagen.
        </p>
        <div class="animated-line" id="magicLine"></div>
    </div>

    <!-- Über mich Sektion -->
    <section id="aboutSection">
        <div class="section-title">
            <i class="fas fa-user-astronaut"></i>
            <span>🚀 Über mich</span>
        </div>
        <p style="font-size: 1.05rem; max-width: 90%; margin-bottom: 0.8rem;">
            Ich kombiniere industrielle Präzision mit modernem Software-Engineering. Meine Mission ist es, komplexe industrielle Prozesse durch Datenanalyse und intuitives Frontend-Design zu optimieren.
        </p>
        <p style="font-size: 1rem; color: #C7D9F5;">
            Mit einem starken Hintergrund in der <strong class="text-highlight" style="color:#F59E0B;">EdTech-Branche</strong> bringe ich die Fähigkeit mit, komplexe technische Konzepte verständlich zu machen und benutzerzentrierte Lösungen zu entwickeln – sei es für Produktions-Dashboards oder interaktive industrielle Schnittstellen.
        </p>
    </section>

    <!-- Tech Arsenal: Frontend & Industrial -->
    <section id="techFrontend">
        <div class="section-title">
            <i class="fab fa-react"></i>
            <span>💻 Frontend & Interaktion (Modern Web)</span>
        </div>
        <div class="tech-grid" id="frontendStack">
            <div class="tech-card"><i class="fab fa-html5" style="color:#E34F26;"></i> HTML5</div>
            <div class="tech-card"><i class="fab fa-css3-alt" style="color:#1572B6;"></i> CSS3</div>
            <div class="tech-card"><i class="fab fa-js" style="color:#F7DF1E;"></i> JavaScript (ES6+)</div>
            <div class="tech-card"><i class="fab fa-js" style="color:#88CE02;"></i> GSAP (GreenSock)</div>
        </div>
    </section>

    <section id="industrialData">
        <div class="section-title">
            <i class="fas fa-industry"></i>
            <span>🏭 Industrial & Data Engineering (Python Ecosystem)</span>
        </div>
        <div class="tech-grid">
            <div class="tech-card"><i class="fab fa-python" style="color:#3776AB;"></i> Python</div>
            <div class="tech-card"><i class="fas fa-chart-line"></i> Pandas</div>
            <div class="tech-card"><i class="fas fa-database"></i> SQL (PostgreSQL, MSSQL)</div>
            <div class="tech-card"><i class="fas fa-chart-simple"></i> Power BI</div>
        </div>
        <div class="protocol-list" style="margin-top: 20px;">
            <span class="protocol-item"><i class="fas fa-plug"></i> Modbus TCP/RTU</span>
            <span class="protocol-item"><i class="fas fa-network-wired"></i> OPC UA</span>
            <span class="protocol-item"><i class="fas fa-microchip"></i> SPS-Datenintegration</span>
        </div>
    </section>

    <!-- Badges / Bibliotheken -->
    <section id="badges">
        <div class="section-title">
            <i class="fas fa-cubes"></i>
            <span>📦 Verwendete Bibliotheken & Werkzeuge</span>
        </div>
        <div class="badge-grid">
            <div class="tech-card"><i class="fab fa-html5"></i> HTML5</div>
            <div class="tech-card"><i class="fab fa-css3-alt"></i> CSS3</div>
            <div class="tech-card"><i class="fab fa-js"></i> JavaScript</div>
            <div class="tech-card"><i class="fas fa-magic"></i> GSAP</div>
            <div class="tech-card"><i class="fab fa-python"></i> Python</div>
            <div class="tech-card"><i class="fas fa-table"></i> Pandas</div>
            <div class="tech-card"><i class="fas fa-database"></i> SQL</div>
            <div class="tech-card"><i class="fas fa-chart-pie"></i> PowerBI</div>
        </div>
    </section>

    <!-- EdTech Experience -->
    <section id="edtech">
        <div class="section-title">
            <i class="fas fa-graduation-cap"></i>
            <span>🎓 EdTech Experience</span>
        </div>
        <div class="edtech-highlight">
            <p><i class="fas fa-lightbulb" style="color:#F59E0B; margin-right: 10px;"></i> Durch meine Erfahrung im EdTech-Bereich habe ich gelernt, wie man:</p>
            <ul style="margin-left: 2rem; margin-top: 0.5rem;">
                <li>📉 <strong>Komplexität reduziert:</strong> Dashboards, die Anwender wirklich verstehen.</li>
                <li>🏗️ <strong>Didaktische Software-Strukturen aufbaut:</strong> Wartbarer, skalierbarer Code.</li>
                <li>👥 <strong>User Experience priorisiert:</strong> Industrielle Software muss nicht kompliziert aussehen.</li>
            </ul>
        </div>
    </section>

    <!-- Aktuelle Projekte -->
    <section id="projects">
        <div class="section-title">
            <i class="fas fa-rocket"></i>
            <span>📈 Aktuelle Projekte</span>
        </div>
        <div class="projects-grid">
            <div class="project-card">
                <i class="fas fa-charging-station"></i>
                <h3>Industrial Energy Dashboard</h3>
                <p>Python & GSAP zur Visualisierung von Energieverbräuchen in Echtzeit.</p>
            </div>
            <div class="project-card">
                <i class="fas fa-chart-line"></i>
                <h3>Automatisierte Reporting-Pipeline</h3>
                <p>SQL-basierte Datenaufbereitung für ESG-Compliance.</p>
            </div>
            <div class="project-card">
                <i class="fas fa-cogs"></i>
                <h3>Prozess-Visualisierung</h3>
                <p>Prototyping mit GSAP zur Darstellung von Maschinen-Zyklen.</p>
            </div>
        </div>
    </section>

    <!-- Connect Sektion -->
    <div class="social-links">
        <a href="https://www.linkedin.com/in/monique-navarro-eng/" class="social-icon" target="_blank"><i class="fab fa-linkedin-in"></i></a>
        <a href="https://github.com/monique-navarro-eng" class="social-icon" target="_blank"><i class="fab fa-github"></i></a>
        <a href="#" class="social-icon" id="fakeMailBtn"><i class="fas fa-envelope"></i></a>
    </div>

    <div class="footer-copyright">
        <i class="far fa-copyright"></i> 2026 Monique Navarro | Passion for Data & Industrial Innovation
    </div>
</div>

<script>
    // GSAP Animationen + ScrollTrigger für Leben
    gsap.registerPlugin(ScrollTrigger, MotionPathPlugin);

    // Hero Animationen beim Laden
    const tl = gsap.timeline();
    tl.from(".gear-wrapper", { duration: 1, scale: 0, rotation: -360, ease: "back.out(1.2)" })
      .from("#mainTitle", { duration: 0.8, y: 50, opacity: 0, ease: "power3.out" }, "-=0.5")
      .from("#subHeadline", { duration: 0.8, x: -40, opacity: 0, ease: "power2.out" }, "-=0.6")
      .from("#missionText", { duration: 0.8, x: 40, opacity: 0, ease: "power2.out" }, "-=0.6")
      .to("#magicLine", { duration: 1.2, width: "30%", ease: "power2.inOut", delay: 0.2 }, "-=0.4");

    // Parallax / Scroll-Effekt auf Sektionen
    gsap.utils.toArray("section").forEach((section, i) => {
        gsap.from(section, {
            scrollTrigger: {
                trigger: section,
                start: "top 85%",
                toggleActions: "play none none reverse",
            },
            opacity: 0,
            y: 60,
            duration: 0.8,
            ease: "power2.out",
        });
    });

    // Cards / Tech-Grid Elemente einzeln animieren
    gsap.utils.toArray(".tech-card").forEach((card, idx) => {
        gsap.from(card, {
            scrollTrigger: {
                trigger: card,
                start: "top 95%",
                toggleActions: "play none none none",
            },
            scale: 0.8,
            opacity: 0,
            duration: 0.4,
            delay: idx * 0.03,
            ease: "back.out(0.8)",
        });
    });

    gsap.utils.toArray(".project-card").forEach((card, idx) => {
        gsap.from(card, {
            scrollTrigger: {
                trigger: card,
                start: "top 90%",
            },
            opacity: 0,
            x: -30,
            duration: 0.5,
            delay: idx * 0.1,
        });
    });

    // Protocol Items animieren
    gsap.utils.toArray(".protocol-item").forEach((item, idx) => {
        gsap.from(item, {
            scrollTrigger: {
                trigger: ".protocol-list",
                start: "top 85%",
            },
            scale: 0.9,
            opacity: 0,
            duration: 0.3,
            delay: idx * 0.05,
            stagger: 0.03,
        });
    });

    // EdTech Highlight pulsieren lassen (dezent)
    gsap.to(".edtech-highlight", {
        scrollTrigger: {
            trigger: ".edtech-highlight",
            start: "top 80%",
        },
        boxShadow: "0 0 12px rgba(245,158,11,0.3)",
        duration: 1,
        repeat: 1,
        yoyo: true,
    });

    // Zusätzlicher dynamischer Effekt für die Zahnrad-Überschrift: beim Scrollen kleiner Dreh-Effekt?
    ScrollTrigger.create({
        trigger: ".hero",
        start: "top top",
        end: "bottom 30%",
        onUpdate: (self) => {
            let rotateVal = self.progress * 360;
            gsap.set(".gear-wrapper img", { rotation: rotateVal * 2 });
        }
    });

    // Hover-Effekte auf tech-cards mit GSAP (optional)
    document.querySelectorAll(".tech-card").forEach(card => {
        card.addEventListener("mouseenter", () => {
            gsap.to(card, { scale: 1.05, backgroundColor: "#1E2A4A", duration: 0.2, ease: "power1.out" });
        });
        card.addEventListener("mouseleave", () => {
            gsap.to(card, { scale: 1, backgroundColor: "#0F172A", duration: 0.2 });
        });
    });

    // Fake Mail Button Konsoleninfo
    document.getElementById("fakeMailBtn")?.addEventListener("click", (e) => {
        e.preventDefault();
        alert("📧 Kontakt: monique.navarro@industrie40.de (Demo) \nLass uns gemeinsam die digitale Industrie gestalten!");
    });

    // dynamische Titelzeile beim Laden
    console.log("%c🚀 Monique Navarro | Industrie 4.0 meets Frontend Magic", "color: #3B82F6; font-size: 1.2rem; font-weight: bold;");
</script>
</body>
</html>
