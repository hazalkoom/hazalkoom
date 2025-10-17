<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohamed Ahmed - Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            min-height: 100vh;
            padding: 20px;
            overflow-x: hidden;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            animation: fadeIn 0.8s ease-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .header {
            text-align: center;
            padding: 40px 20px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            margin-bottom: 30px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            animation: slideDown 0.6s ease-out;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .wave {
            animation: wave 2s infinite;
            display: inline-block;
            font-size: 3em;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-20deg); }
        }

        h1 {
            font-size: 2.5em;
            margin: 20px 0 10px;
            background: linear-gradient(45deg, #fff, #a8edea);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .tagline {
            font-size: 1.2em;
            opacity: 0.9;
            margin-bottom: 15px;
        }

        .intro {
            font-size: 1em;
            line-height: 1.6;
            opacity: 0.85;
        }

        .section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 25px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            animation: fadeInUp 0.6s ease-out backwards;
        }

        .section:nth-child(2) { animation-delay: 0.1s; }
        .section:nth-child(3) { animation-delay: 0.2s; }
        .section:nth-child(4) { animation-delay: 0.3s; }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        h2 {
            font-size: 1.8em;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin-top: 15px;
        }

        .skill-category {
            margin-bottom: 25px;
        }

        .skill-category h3 {
            font-size: 1.2em;
            margin-bottom: 15px;
            opacity: 0.9;
        }

        .skill-badge {
            background: rgba(255, 255, 255, 0.2);
            padding: 10px 15px;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
            font-weight: 500;
        }

        .skill-badge:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .projects-section {
            text-align: center;
        }

        .github-button {
            display: inline-block;
            background: linear-gradient(45deg, #24292e, #000);
            color: #fff;
            padding: 15px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-size: 1.1em;
            font-weight: bold;
            margin-top: 20px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
        }

        .github-button:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 6px 25px rgba(0, 0, 0, 0.4);
        }

        .learning-section {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.15), rgba(255, 255, 255, 0.05));
        }

        .learning-items {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
        }

        .learning-item {
            background: rgba(255, 255, 255, 0.2);
            padding: 12px 20px;
            border-radius: 25px;
            font-weight: 500;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 25px;
            flex-wrap: wrap;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(255, 255, 255, 0.2);
            padding: 12px 25px;
            border-radius: 30px;
            text-decoration: none;
            color: #fff;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .floating {
            animation: floating 3s ease-in-out infinite;
        }

        @keyframes floating {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        @media (max-width: 768px) {
            h1 { font-size: 2em; }
            .skills-grid { grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <span class="wave">👋</span>
            <h1>Hi, I'm Mohamed Ahmed!</h1>
            <p class="tagline">College Student | Full Stack Developer | Tech Enthusiast</p>
            <p class="intro">Passionate about creating practical and user-friendly applications. I focus on building clean, functional, and visually appealing web applications with modern technologies.</p>
        </div>

        <div class="section">
            <h2>🛠️ My Skills</h2>
            
            <div class="skill-category">
                <h3>Programming Languages</h3>
                <div class="skills-grid">
                    <div class="skill-badge">Python</div>
                    <div class="skill-badge">JavaScript</div>
                    <div class="skill-badge">TypeScript</div>
                    <div class="skill-badge">C#</div>
                </div>
            </div>

            <div class="skill-category">
                <h3>Frontend Development</h3>
                <div class="skills-grid">
                    <div class="skill-badge">HTML5</div>
                    <div class="skill-badge">CSS3</div>
                    <div class="skill-badge">Bootstrap</div>
                    <div class="skill-badge">Angular</div>
                </div>
            </div>

            <div class="skill-category">
                <h3>Backend Development</h3>
                <div class="skills-grid">
                    <div class="skill-badge">Django</div>
                    <div class="skill-badge">Django REST</div>
                    <div class="skill-badge">Node.js</div>
                    <div class="skill-badge">Express.js</div>
                </div>
            </div>

            <div class="skill-category">
                <h3>Database & Data</h3>
                <div class="skills-grid">
                    <div class="skill-badge">SQL</div>
                    <div class="skill-badge">MySQL</div>
                    <div class="skill-badge">NoSQL</div>
                    <div class="skill-badge">Pandas</div>
                </div>
            </div>
        </div>

        <div class="section projects-section floating">
            <h2>🌟 My Projects</h2>
            <p style="opacity: 0.9; margin-bottom: 10px;">Check out my work and contributions on GitHub</p>
            <a href="https://github.com/hazalkoom" target="_blank" class="github-button">
                View My GitHub Projects →
            </a>
        </div>

        <div class="section learning-section">
            <h2>🚀 Currently Exploring</h2>
            <div class="learning-items">
                <div class="learning-item">Advanced TypeScript</div>
                <div class="learning-item">Angular Deep Dive</div>
                <div class="learning-item">Microservices Architecture</div>
                <div class="learning-item">Data Analysis with Pandas</div>
            </div>
        </div>

        <div class="section">
            <h2>📫 Connect With Me</h2>
            <div class="social-links">
                <a href="https://www.linkedin.com/in/mohamed-ahmed-mahmoud-766912268/" target="_blank" class="social-link">
                    <span>💼</span> LinkedIn
                </a>
                <a href="https://github.com/hazalkoom/" target="_blank" class="social-link">
                    <span>💻</span> GitHub
                </a>
                <a href="https://www.instagram.com/mohawksq11/" target="_blank" class="social-link">
                    <span>📸</span> Instagram
                </a>
            </div>
        </div>
    </div>
</body>
</html>
