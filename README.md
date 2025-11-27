<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aryan Dhiman - Full Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>
    <style>
        :root {
            --primary: #0ea5e9;
            --secondary: #7e22ce;
            --dark: #0f172a;
            --darker: #020617;
            --light: #f8fafc;
            --gray: #64748b;
            --success: #10b981;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--darker);
            color: var(--light);
            overflow-x: hidden;
            line-height: 1.6;
        }
        
        #particles-js {
            position: fixed;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            padding: 100px 0 60px;
            text-align: center;
            position: relative;
        }
        
        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 4px solid var(--primary);
            margin: 0 auto 25px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 0 30px rgba(14, 165, 233, 0.4);
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }
        
        .profile-img::before {
            content: '';
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            background: linear-gradient(45deg, var(--primary), var(--secondary), var(--primary));
            z-index: -1;
            border-radius: 50%;
            animation: rotate 10s linear infinite;
        }
        
        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .profile-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 50%;
            background: var(--dark);
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 15px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            display: inline-block;
        }
        
        .tagline {
            font-size: 1.5rem;
            color: var(--gray);
            margin-bottom: 30px;
        }
        
        /* Section Styles */
        section {
            padding: 80px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        h2 {
            font-size: 2.5rem;
            margin-bottom: 40px;
            text-align: center;
            position: relative;
        }
        
        h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border-radius: 2px;
        }
        
        /* About Section */
        .about-content {
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
            align-items: center;
            justify-content: center;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
        }
        
        .about-text p {
            margin-bottom: 20px;
            font-size: 1.1rem;
        }
        
        .highlight {
            color: var(--primary);
            font-weight: bold;
        }
        
        /* Stats Section */
        .stats-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }
        
        .stat-card {
            background: rgba(15, 23, 42, 0.7);
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            min-width: 200px;
            flex: 1;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            backdrop-filter: blur(10px);
        }
        
        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--primary);
            margin-bottom: 10px;
        }
        
        .stat-label {
            color: var(--gray);
            font-size: 1rem;
        }
        
        /* Skills Section */
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            justify-content: center;
        }
        
        .skill-category {
            background: rgba(15, 23, 42, 0.7);
            border-radius: 15px;
            padding: 30px;
            flex: 1;
            min-width: 300px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }
        
        .skill-category h3 {
            margin-bottom: 20px;
            color: var(--primary);
            font-size: 1.5rem;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
            gap: 15px;
        }
        
        .skill-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            transition: transform 0.3s;
        }
        
        .skill-item:hover {
            transform: scale(1.1);
        }
        
        .skill-icon {
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            margin-bottom: 8px;
            font-size: 1.8rem;
        }
        
        .skill-name {
            font-size: 0.8rem;
            text-align: center;
        }
        
        /* Social Links */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }
        
        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 255, 255, 0.05);
            color: var(--light);
            font-size: 1.5rem;
            transition: all 0.3s;
            text-decoration: none;
        }
        
        .social-link:hover {
            background: var(--primary);
            transform: translateY(-5px);
        }
        
        /* Quote Section */
        .quote-container {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
            padding: 40px;
            background: rgba(15, 23, 42, 0.7);
            border-radius: 15px;
            border-left: 4px solid var(--primary);
            backdrop-filter: blur(10px);
        }
        
        .quote {
            font-size: 1.5rem;
            font-style: italic;
            margin-bottom: 20px;
            color: var(--light);
        }
        
        .author {
            color: var(--primary);
            font-weight: bold;
        }
        
        /* Footer */
        footer {
            padding: 40px 0;
            text-align: center;
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        /* Animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s, transform 0.8s;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            section {
                padding: 60px 0;
            }
            
            .profile-img {
                width: 150px;
                height: 150px;
            }
        }
        
        /* Toggle Theme Button */
        .theme-toggle {
            position: fixed;
            top: 20px;
            right: 20px;
            background: rgba(15, 23, 42, 0.7);
            border: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--light);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            z-index: 100;
            backdrop-filter: blur(10px);
            transition: all 0.3s;
        }
        
        .theme-toggle:hover {
            background: var(--primary);
        }
        
        /* Light Theme */
        body.light-theme {
            background-color: #f1f5f9;
            color: #1e293b;
        }
        
        body.light-theme .stat-card,
        body.light-theme .skill-category,
        body.light-theme .quote-container {
            background: rgba(255, 255, 255, 0.7);
            color: #1e293b;
            border: 1px solid rgba(0, 0, 0, 0.1);
        }
        
        body.light-theme .social-link {
            background: rgba(0, 0, 0, 0.05);
            color: #1e293b;
        }
        
        body.light-theme .tagline,
        body.light-theme .stat-label {
            color: #64748b;
        }
        
        body.light-theme section {
            border-bottom: 1px solid rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>
    <!-- Particles Background -->
    <div id="particles-js"></div>
    
    <!-- Theme Toggle -->
    <div class="theme-toggle" id="themeToggle">
        <i class="fas fa-moon"></i>
    </div>
    
    <!-- Header Section -->
    <header>
        <div class="container">
            <div class="profile-img">
                <!-- Placeholder for profile image -->
                <div style="width:100%;height:100%;background:linear-gradient(45deg, #0ea5e9, #7e22ce);display:flex;align-items:center;justify-content:center;color:white;font-size:3rem;">
                    AD
                </div>
            </div>
            <h1>Aryan Dhiman</h1>
            <p class="tagline">Full Stack Developer & Tech Enthusiast</p>
            <div class="social-links">
                <a href="https://www.linkedin.com/in/aryan-dhiman-2605ad" class="social-link" target="_blank">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="https://github.com/aryan-26-prog" class="social-link" target="_blank">
                    <i class="fab fa-github"></i>
                </a>
                <a href="mailto:aryandhiman2605@gmail.com" class="social-link">
                    <i class="fas fa-envelope"></i>
                </a>
                <a href="https://instagram.com/aryandhiman_01" class="social-link" target="_blank">
                    <i class="fab fa-instagram"></i>
                </a>
            </div>
        </div>
    </header>
    
    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2>About Me</h2>
            <div class="about-content">
                <div class="about-text fade-in">
                    <p>Hello! I'm <span class="highlight">Aryan Dhiman</span>, a passionate full-stack developer with a love for creating innovative web solutions.</p>
                    <p>I'm currently exploring <span class="highlight">MERN stack, Django, AI</span> and working on real-life projects that solve practical problems.</p>
                    <p>When I'm not coding, you can find me learning new technologies, contributing to open-source projects, or exploring the latest trends in web development.</p>
                    <p>I believe in <span class="highlight">"learning by doing"</span> and constantly challenging myself to grow both personally and professionally.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Stats Section -->
    <section id="stats">
        <div class="container">
            <h2>GitHub Statistics</h2>
            <div class="stats-container">
                <div class="stat-card fade-in">
                    <div class="stat-number" id="repos">24</div>
                    <div class="stat-label">Repositories</div>
                </div>
                <div class="stat-card fade-in">
                    <div class="stat-number" id="commits">187</div>
                    <div class="stat-label">Commits</div>
                </div>
                <div class="stat-card fade-in">
                    <div class="stat-number" id="streak">42</div>
                    <div class="stat-label">Day Streak</div>
                </div>
                <div class="stat-card fade-in">
                    <div class="stat-number" id="contributions">126</div>
                    <div class="stat-label">Contributions</div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <h2>Tech Stack & Tools</h2>
            <div class="skills-container">
                <div class="skill-category fade-in">
                    <h3>Frontend</h3>
                    <div class="skills-grid">
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fab fa-react"></i>
                            </div>
                            <div class="skill-name">React</div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fab fa-js"></i>
                            </div>
                            <div class="skill-name">JavaScript</div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fab fa-html5"></i>
                            </div>
                            <div class="skill-name">HTML5</div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fab fa-css3-alt"></i>
                            </div>
                            <div class="skill-name">CSS3</div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category fade-in">
                    <h3>Backend</h3>
                    <div class="skills-grid">
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fab fa-node-js"></i>
                            </div>
                            <div class="skill-name">Node.js</div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fab fa-python"></i>
                            </div>
                            <div class="skill-name">Python</div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fas fa-database"></i>
                            </div>
                            <div class="skill-name">MongoDB</div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fab fa-php"></i>
                            </div>
                            <div class="skill-name">PHP</div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category fade-in">
                    <h3>Tools</h3>
                    <div class="skills-grid">
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fab fa-git-alt"></i>
                            </div>
                            <div class="skill-name">Git</div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fab fa-github"></i>
                            </div>
                            <div class="skill-name">GitHub</div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fas fa-code"></i>
                            </div>
                            <div class="skill-name">VS Code</div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-icon">
                                <i class="fas fa-rocket"></i>
                            </div>
                            <div class="skill-name">Vite</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Quote Section -->
    <section id="quote">
        <div class="container">
            <div class="quote-container fade-in">
                <p class="quote">"I break things while learning… then learn how to fix them better!"</p>
                <p class="author">- Aryan Dhiman</p>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <p>© 2023 Aryan Dhiman. All rights reserved.</p>
            <p>Made with ❤️ and a lot of ☕</p>
        </div>
    </footer>
    
    <script>
        // Initialize Particles.js
        particlesJS('particles-js', {
            particles: {
                number: { value: 80, density: { enable: true, value_area: 800 } },
                color: { value: "#0ea5e9" },
                shape: { type: "circle" },
                opacity: { value: 0.5, random: true },
                size: { value: 3, random: true },
                line_linked: {
                    enable: true,
                    distance: 150,
                    color: "#7e22ce",
                    opacity: 0.4,
                    width: 1
                },
                move: {
                    enable: true,
                    speed: 2,
                    direction: "none",
                    random: true,
                    straight: false,
                    out_mode: "out",
                    bounce: false
                }
            },
            interactivity: {
                detect_on: "canvas",
                events: {
                    onhover: { enable: true, mode: "repulse" },
                    onclick: { enable: true, mode: "push" },
                    resize: true
                }
            }
        });
        
        // Scroll animations
        const fadeElements = document.querySelectorAll('.fade-in');
        
        const fadeInOnScroll = () => {
            fadeElements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                const elementVisible = 150;
                
                if (elementTop < window.innerHeight - elementVisible) {
                    element.classList.add('visible');
                }
            });
        };
        
        window.addEventListener('scroll', fadeInOnScroll);
        window.addEventListener('load', fadeInOnScroll);
        
        // Theme toggle functionality
        const themeToggle = document.getElementById('themeToggle');
        const themeIcon = themeToggle.querySelector('i');
        
        themeToggle.addEventListener('click', () => {
            document.body.classList.toggle('light-theme');
            
            if (document.body.classList.contains('light-theme')) {
                themeIcon.classList.remove('fa-moon');
                themeIcon.classList.add('fa-sun');
            } else {
                themeIcon.classList.remove('fa-sun');
                themeIcon.classList.add('fa-moon');
            }
        });
        
        // Animated counter for stats
        const counters = document.querySelectorAll('.stat-number');
        const speed = 200;
        
        const animateCounters = () => {
            counters.forEach(counter => {
                const target = +counter.getAttribute('data-target') || 
                    (counter.id === 'repos' ? 24 : 
                     counter.id === 'commits' ? 187 : 
                     counter.id === 'streak' ? 42 : 126);
                
                const count = +counter.innerText;
                const increment = target / speed;
                
                if (count < target) {
                    counter.innerText = Math.ceil(count + increment);
                    setTimeout(animateCounters, 10);
                } else {
                    counter.innerText = target;
                }
            });
        };
        
        // Start counter animation when stats section is in view
        const statsSection = document.getElementById('stats');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    animateCounters();
                    observer.unobserve(entry.target);
                }
            });
        }, { threshold: 0.5 });
        
        observer.observe(statsSection);
    </script>
</body>
</html>
