<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Faizan Fareed - Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #8a2be2;
            --secondary: #00b4d8;
            --accent: #f72585;
            --dark: #121212;
            --darker: #0a0a0a;
            --light: #f8f9fa;
            --gray: #2d2d2d;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, var(--darker) 0%, var(--dark) 100%);
            color: var(--light);
            line-height: 1.6;
            padding: 0;
            margin: 0;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Section */
        .header {
            text-align: center;
            padding: 80px 20px 60px;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at top right, var(--primary) 0%, transparent 70%);
            opacity: 0.2;
            z-index: -1;
        }
        
        .header h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            display: inline-block;
            animation: fadeIn 1s ease;
        }
        
        .header h3 {
            font-size: 1.8rem;
            font-weight: 400;
            margin-bottom: 20px;
            color: var(--secondary);
            animation: fadeIn 1.5s ease;
        }
        
        .tagline {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
            margin-top: 20px;
            animation: fadeIn 2s ease;
        }
        
        .tag {
            background: rgba(138, 43, 226, 0.1);
            border: 1px solid var(--primary);
            padding: 8px 15px;
            border-radius: 50px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: var(--transition);
        }
        
        .tag:hover {
            background: rgba(138, 43, 226, 0.2);
            transform: translateY(-3px);
        }
        
        /* Section Styling */
        .section {
            padding: 60px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            font-size: 2.2rem;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--primary), transparent);
        }
        
        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }
        
        .about-text {
            font-size: 1.1rem;
        }
        
        .highlight {
            color: var(--secondary);
            font-weight: 600;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
            gap: 15px;
        }
        
        .skill-item {
            background: var(--gray);
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            transition: var(--transition);
            border: 1px solid transparent;
        }
        
        .skill-item:hover {
            border-color: var(--primary);
            transform: translateY(-5px);
        }
        
        /* Stats Section */
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: var(--transition);
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 25px;
        }
        
        .project-card {
            background: linear-gradient(145deg, var(--gray), var(--dark));
            border-radius: 12px;
            overflow: hidden;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-title {
            font-size: 1.4rem;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .project-desc {
            margin-bottom: 15px;
            color: #ccc;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }
        
        .tech-tag {
            background: rgba(0, 180, 216, 0.1);
            color: var(--secondary);
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        .project-link {
            display: inline-block;
            color: var(--primary);
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
        }
        
        .project-link:hover {
            color: var(--secondary);
        }
        
        /* Contact Section */
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .contact-btn {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 12px 25px;
            background: rgba(138, 43, 226, 0.1);
            border: 1px solid var(--primary);
            border-radius: 50px;
            color: var(--light);
            text-decoration: none;
            transition: var(--transition);
            font-weight: 500;
        }
        
        .contact-btn:hover {
            background: rgba(138, 43, 226, 0.3);
            transform: translateY(-3px);
        }
        
        /* Snake Animation */
        .snake-container {
            margin: 40px 0;
            text-align: center;
        }
        
        .snake-placeholder {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 40px;
            border: 1px dashed var(--primary);
            color: #999;
        }
        
        /* Footer */
        .footer {
            text-align: center;
            padding: 30px 0;
            color: #999;
            font-size: 0.9rem;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .animated {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.5s ease, transform 0.5s ease;
        }
        
        .in-view {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5rem;
            }
            
            .header h3 {
                font-size: 1.4rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .stats-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <header class="header">
            <h1>Hi, I'm Faizan Fareed</h1>
            <h3>Software Engineer | Full Stack Developer | Tech Explorer</h3>
            <div class="tagline">
                <div class="tag"><i class="fas fa-graduation-cap"></i> Software Engineering Student</div>
                <div class="tag"><i class="fas fa-code"></i> Full Stack Developer</div>
                <div class="tag"><i class="fas fa-rocket"></i> Tech Enthusiast</div>
            </div>
        </header>
        
        <!-- About Section -->
        <section class="section">
            <h2 class="section-title animated">About Me</h2>
            <div class="about-content">
                <div class="about-text animated">
                    <p>I'm a passionate software engineering student with a focus on building <span class="highlight">real-world projects</span> that solve practical problems. I love turning ideas into reality through clean and scalable code.</p>
                    <p>Currently, I'm expanding my skills in <span class="highlight">Laravel & Advanced Python</span> while exploring the fascinating worlds of AI, Web Development, and Cybersecurity.</p>
                    <p>When I'm not coding, you can find me learning about new technologies, contributing to open source, or exploring the latest in tech innovation.</p>
                </div>
                <div class="skills-grid animated">
                    <div class="skill-item">JavaScript</div>
                    <div class="skill-item">Python</div>
                    <div class="skill-item">PHP</div>
                    <div class="skill-item">Laravel</div>
                    <div class="skill-item">React</div>
                    <div class="skill-item">Node.js</div>
                    <div class="skill-item">HTML/CSS</div>
                    <div class="skill-item">MySQL</div>
                </div>
            </div>
        </section>
        
        <!-- Stats Section -->
        <section class="section">
            <h2 class="section-title animated">GitHub Stats</h2>
            <div class="stats-container">
                <div class="stat-card animated">
                    <h3>GitHub Statistics</h3>
                    <img src="https://github-readme-stats.vercel.app/api?username=faizanfareed275&show_icons=true&theme=tokyonight&hide_border=true" alt="GitHub Stats" style="width: 100%">
                </div>
                <div class="stat-card animated">
                    <h3>Streak Stats</h3>
                    <img src="https://github-readme-streak-stats.herokuapp.com/?user=faizanfareed275&theme=tokyonight&hide_border=true" alt="Streak Stats" style="width: 100%">
                </div>
                <div class="stat-card animated">
                    <h3>Top Languages</h3>
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=faizanfareed275&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" style="width: 100%">
                </div>
            </div>
            
            <div class="snake-container animated">
                <div class="snake-placeholder">
                    <p>GitHub Contribution Snake Animation Would Appear Here</p>
                    <p><small>(Note: This is a placeholder. The actual animation requires SVG generated by GitHub)</small></p>
                </div>
            </div>
        </section>
        
        <!-- Projects Section -->
        <section class="section">
            <h2 class="section-title animated">Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card animated">
                    <div class="project-content">
                        <h3 class="project-title">Operation App</h3>
                        <div class="project-tech">
                            <span class="tech-tag">JavaScript</span>
                        </div>
                        <p class="project-desc">A simple calculator & operations-based app with clean UI and intuitive user experience.</p>
                        <a href="https://github.com/faizanfareed275/Operation_App" class="project-link">View Project →</a>
                    </div>
                </div>
                
                <div class="project-card animated">
                    <div class="project-content">
                        <h3 class="project-title">Library Management System</h3>
                        <div class="project-tech">
                            <span class="tech-tag">PHP</span>
                            <span class="tech-tag">Laravel</span>
                            <span class="tech-tag">MySQL</span>
                        </div>
                        <p class="project-desc">Complete Library System with login/signup, admin dashboard & user management features.</p>
                        <a href="https://github.com/faizanfareed275/Library-Management-System" class="project-link">View Project →</a>
                    </div>
                </div>
                
                <div class="project-card animated">
                    <div class="project-content">
                        <h3 class="project-title">AI eCommerce Analyzer</h3>
                        <div class="project-tech">
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">Data Science</span>
                            <span class="tech-tag">Web Scraping</span>
                        </div>
                        <p class="project-desc">Scrapes eCommerce platforms to analyze and identify top-selling products using AI techniques.</p>
                        <a href="https://github.com/faizanfareed275/ai_best_seller_analyzer" class="project-link">View Project →</a>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Contact Section -->
        <section class="section">
            <h2 class="section-title animated">Connect With Me</h2>
            <div class="contact-links">
                <a href="https://www.linkedin.com/in/faizan-fareed/" class="contact-btn animated">
                    <i class="fab fa-linkedin"></i> LinkedIn
                </a>
                <a href="mailto:faizan@example.com" class="contact-btn animated">
                    <i class="fas fa-envelope"></i> Email
                </a>
                <a href="https://your-website.com" class="contact-btn animated">
                    <i class="fas fa-globe"></i> Portfolio
                </a>
                <a href="https://github.com/faizanfareed275" class="contact-btn animated">
                    <i class="fab fa-github"></i> GitHub
                </a>
            </div>
        </section>
        
        <!-- Footer -->
        <footer class="footer">
            <p>⭐️ From <a href="https://github.com/faizanfareed275" style="color: var(--primary); text-decoration: none;">faizanfareed275</a></p>
            <p>Made with ❤️ and ☕</p>
        </footer>
    </div>

    <script>
        // Animation on scroll
        document.addEventListener('DOMContentLoaded', function() {
            const animatedElements = document.querySelectorAll('.animated');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        setTimeout(() => {
                            entry.target.classList.add('in-view');
                        }, 100);
                    }
                });
            }, {
                threshold: 0.1
            });
            
            animatedElements.forEach(element => {
                observer.observe(element);
            });
        });
    </script>
</body>
</html>
