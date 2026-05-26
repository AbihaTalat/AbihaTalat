<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Abiha Talat | Portfolio</title>

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            overflow-x: hidden;
        }

        /* HERO SECTION */

        .hero {
            width: 100%;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            overflow: hidden;
            padding: 40px 20px;
        }

        .container {
            text-align: center;
            position: relative;
            z-index: 10;
            max-width: 1000px;
        }

        .name-wrapper {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .first-name,
        .last-name {
            font-size: clamp(60px, 10vw, 120px);
            font-weight: 700;
            letter-spacing: 8px;
            text-shadow:
                0 0 20px rgba(255, 255, 255, 0.8),
                0 0 40px rgba(255, 200, 87, 0.5);
            animation: float 3s ease-in-out infinite,
                       glow 2s ease-in-out infinite;
        }

        .last-name {
            animation-delay: 0.3s;
        }

        .subtitle {
            margin-top: 25px;
            font-size: 20px;
            letter-spacing: 3px;
            color: rgba(255,255,255,0.9);
            animation: slideIn 1s ease-out;
        }

        .character-container {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-top: 45px;
            flex-wrap: wrap;
        }

        .character {
            font-size: 70px;
            animation: float-character 3s ease-in-out infinite;
        }

        .character:nth-child(2) {
            animation-delay: 0.2s;
        }

        .character:nth-child(3) {
            animation-delay: 0.4s;
        }

        /* CONTENT */

        .content-section {
            max-width: 1100px;
            margin: auto;
            padding: 80px 25px;
            position: relative;
            z-index: 2;
        }

        .card {
            background: rgba(255,255,255,0.08);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255,255,255,0.15);
            border-radius: 24px;
            padding: 35px;
            margin-bottom: 35px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            transition: 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        h2 {
            font-size: 32px;
            margin-bottom: 20px;
        }

        p {
            line-height: 1.8;
            font-size: 17px;
            color: rgba(255,255,255,0.9);
        }

        /* SOCIALS */

        .socials {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }

        .socials a {
            text-decoration: none;
            color: white;
            background: rgba(255,255,255,0.12);
            padding: 12px 20px;
            border-radius: 12px;
            transition: 0.3s ease;
            border: 1px solid rgba(255,255,255,0.1);
        }

        .socials a:hover {
            background: rgba(255,255,255,0.25);
            transform: scale(1.05);
        }

        /* TECH STACK */

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 14px;
            margin-top: 20px;
        }

        .tech {
            padding: 10px 18px;
            border-radius: 50px;
            background: rgba(255,255,255,0.12);
            border: 1px solid rgba(255,255,255,0.1);
            font-size: 14px;
            transition: 0.3s ease;
        }

        .tech:hover {
            transform: scale(1.08);
            background: rgba(255,255,255,0.2);
        }

        /* GITHUB STATS */

        .stats {
            display: flex;
            flex-direction: column;
            gap: 20px;
            margin-top: 25px;
        }

        .stats img {
            width: 100%;
            border-radius: 20px;
        }

        /* STARS */

        .stars-container,
        .glitter-container {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            overflow: hidden;
        }

        .star {
            position: absolute;
            font-size: 24px;
            animation: float-star 4s ease-in-out infinite;
        }

        .glitter {
            position: absolute;
            width: 6px;
            height: 6px;
            background: radial-gradient(circle, #ffff00, #ffc857);
            border-radius: 50%;
            animation: glitter-sparkle 1.5s ease-in-out infinite;
            box-shadow: 0 0 10px rgba(255,255,0,0.8);
        }

        /* ANIMATIONS */

        @keyframes float {
            0%, 100% {
                transform: translateY(0px) scale(1);
            }
            50% {
                transform: translateY(-20px) scale(1.05);
            }
        }

        @keyframes glow {
            0%, 100% {
                color: white;
            }
            50% {
                color: #ffc857;
            }
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes float-character {
            0%, 100% {
                transform: translateY(0) rotate(0deg);
            }
            50% {
                transform: translateY(-15px) rotate(5deg);
            }
        }

        @keyframes float-star {
            0% {
                opacity: 0;
                transform: translateY(-100px);
            }
            50% {
                opacity: 1;
            }
            100% {
                opacity: 0;
                transform: translateY(100px) translateX(30px);
            }
        }

        @keyframes glitter-sparkle {
            0%, 100% {
                opacity: 0;
                transform: scale(0);
            }
            50% {
                opacity: 1;
                transform: scale(1);
            }
        }

        /* MOBILE */

        @media(max-width: 768px) {
            .card {
                padding: 25px;
            }

            h2 {
                font-size: 26px;
            }

            p {
                font-size: 15px;
            }

            .character {
                font-size: 50px;
            }
        }
    </style>
</head>

<body>

    <div class="stars-container" id="starsContainer"></div>
    <div class="glitter-container" id="glitterContainer"></div>

    <!-- HERO -->
    <section class="hero">
        <div class="container">

            <div class="name-wrapper">
                <h1 class="first-name">ABIHA</h1>
                <h1 class="last-name">TALAT</h1>
            </div>

            <p class="subtitle">Developer • Builder • Creator</p>

            <div class="character-container">
                <div class="character">🐱</div>
                <div class="character">⚡</div>
                <div class="character">🌟</div>
            </div>

        </div>
    </section>

    <!-- ABOUT -->
    <section class="content-section">

        <div class="card">
            <h2>💫 About Me</h2>

            <p>
                Curious by nature and driven by understanding, I enjoy exploring ideas deeply
                and learning through building. I value growth, creativity, and independence,
                and I tend to approach challenges with a “figure it out” mindset rather than
                fear of failure.
            </p>
        </div>

        <!-- SOCIALS -->

        <div class="card">
            <h2>🌐 Socials</h2>

            <div class="socials">
                <a href="https://discord.gg/hVnbyJy5" target="_blank">Discord</a>

                <a href="https://www.linkedin.com/in/abiha-talat-145417371/"
                   target="_blank">
                   LinkedIn
                </a>

                <a href="mailto:works.abihat461@gmail.com">
                    Email
                </a>
            </div>
        </div>

        <!-- TECH STACK -->

        <div class="card">
            <h2>💻 Tech Stack</h2>

            <div class="tech-stack">
                <div class="tech">C++</div>
                <div class="tech">JavaScript</div>
                <div class="tech">HTML5</div>
                <div class="tech">PowerShell</div>
                <div class="tech">Oracle</div>
                <div class="tech">Vite</div>
                <div class="tech">React Native</div>
                <div class="tech">React</div>
                <div class="tech">Node.js</div>
                <div class="tech">Nodemon</div>
                <div class="tech">MySQL</div>
                <div class="tech">MongoDB</div>
                <div class="tech">Microsoft SQL Server</div>
                <div class="tech">Canva</div>
                <div class="tech">Adobe Lightroom</div>
                <div class="tech">Git</div>
                <div class="tech">GitHub</div>
            </div>
        </div>

        <!-- GITHUB STATS -->

        <div class="card">
            <h2>📊 GitHub Stats</h2>

            <div class="stats">

                <img
                    src="https://github-readme-stats.shion.dev/api?username=AbihaTalat&theme=radical&hide_border=false&include_all_commits=true&count_private=false"
                    alt="GitHub Stats"
                />

                <img
                    src="https://streak-stats.demolab.com/?user=AbihaTalat&theme=radical&hide_border=false"
                    alt="GitHub Streak"
                />

                <img
                    src="https://github-readme-stats.shion.dev/api/top-langs/?username=AbihaTalat&theme=radical&hide_border=false&include_all_commits=true&count_private=false&layout=compact"
                    alt="Top Languages"
                />

            </div>
        </div>

        <!-- QUOTE -->

        <div class="card">
            <h2>✍️ Random Dev Quote</h2>

            <img
                src="https://quotes-github-readme.vercel.app/api?type=vertical&theme=radical"
                alt="Dev Quote"
                style="width:100%; border-radius:20px;"
            />
        </div>

        <!-- TOP REPOS -->

        <div class="card">
            <h2>🔝 Top Contributed Repo</h2>

            <img
                src="https://github-contributor-stats.vercel.app/api?username=AbihaTalat&limit=5&theme=dark&combine_all_yearly_contributions=true"
                alt="Top Repo"
                style="width:100%; border-radius:20px;"
            />
        </div>

    </section>

    <script>
        // Floating stars
        const starsContainer = document.getElementById('starsContainer');
        const starEmojis = ['⭐', '✨', '💫', '🌠'];

        function createStar() {
            const star = document.createElement('div');

            star.className = 'star';
            star.textContent =
                starEmojis[Math.floor(Math.random() * starEmojis.length)];

            star.style.left = Math.random() * 100 + '%';
            star.style.top = Math.random() * 20 + '%';
            star.style.animationDuration =
                (2 + Math.random() * 2) + 's';

            starsContainer.appendChild(star);

            setTimeout(() => {
                star.remove();
            }, 6000);
        }

        setInterval(createStar, 400);

        // Glitter
        const glitterContainer =
            document.getElementById('glitterContainer');

        function createGlitter() {
            const glitter = document.createElement('div');

            glitter.className = 'glitter';

            glitter.style.left = Math.random() * 100 + '%';
            glitter.style.top = Math.random() * 100 + '%';

            glitterContainer.appendChild(glitter);

            setTimeout(() => {
                glitter.remove();
            }, 3000);
        }

        setInterval(createGlitter, 200);
    </script>

</body>
</html>
