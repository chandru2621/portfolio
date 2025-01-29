<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chandru Mani | Full Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #2980b9;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', sans-serif;
        }

        body {
            line-height: 1.6;
            color: var(--dark);
        }

        /* Header Styles */
        .hero {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 4rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: slideUp 1s ease;
        }

        .contact-bar {
            background: rgba(255,255,255,0.1);
            padding: 1rem;
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
            border-radius: 10px;
            margin: 2rem auto;
            max-width: 800px;
        }

        .contact-bar a {
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: transform 0.3s ease;
        }

        .contact-bar a:hover {
            transform: translateY(-3px);
        }

        /* Section Styles */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .section {
            margin: 4rem 0;
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.6s ease;
        }

        .section.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .section-title {
            color: var(--secondary);
            border-bottom: 3px solid var(--secondary);
            padding-bottom: 0.5rem;
            margin-bottom: 2rem;
            font-size: 2rem;
            position: relative;
        }

        /* Experience Cards */
        .experience-card {
            background: white;
            padding: 2rem;
            margin: 1.5rem 0;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .experience-card:hover {
            transform: translateY(-5px);
        }

        /* Project Grid */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: white;
            border-radius: 10px;
            padding: 1.5rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--secondary);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .project-card:hover::before {
            transform: scaleX(1);
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
        }

        .skill-item {
            background: var(--light);
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .skill-item:hover {
            background: var(--secondary);
            color: white;
        }

        /* Animations */
        @keyframes slideUp {
            from { transform: translateY(50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <header class="hero">
        <h1>Chandru Mani</h1>
        <p>Full Stack Developer & Tech Enthusiast</p>
        
        <div class="contact-bar">
            <a href="mailto:chandrumani260@gmail.com">
                <i class="fas fa-envelope"></i> Email
            </a>
            <a href="tel:+919361464234">
                <i class="fas fa-phone"></i> +91 9361464234
            </a>
            <a href="https://github.com/chandru2621" target="_blank">
                <i class="fab fa-github"></i> GitHub
            </a>
            <a href="https://www.linkedin.com/in/chandru-mani-5aa463345" target="_blank">
                <i class="fab fa-linkedin"></i> LinkedIn
            </a>
        </div>
    </header>

    <main class="container">
        <section class="section" id="about">
            <h2 class="section-title">About Me</h2>
            <p class="lead">Passionate Full Stack Developer with expertise in Python and modern web technologies. Focused on building dynamic applications and collaborating with teams to create impactful web experiences.</p>
        </section>

        <section class="section" id="experience">
            <h2 class="section-title">Professional Journey</h2>
            <div class="experience-card">
                <h3>Full Stack Developer Intern</h3>
                <div class="meta">
                    <span class="company">DLK Company</span>
                    <span class="duration">Aug 2022</span>
                </div>
                <ul class="achievements">
                    <li>Developed Python-based backend systems handling 1000+ daily transactions</li>
                    <li>Implemented REST APIs improving system efficiency by 40%</li>
                </ul>
            </div>
            <!-- Add other experiences -->
        </section>

        <section class="section" id="projects">
            <h2 class="section-title">Featured Projects</h2>
            <div class="project-grid">
                <div class="project-card">
                    <h3>Book a Doctor (MERN)</h3>
                    <p>Medical appointment system with real-time updates</p>
                    <div class="tech-stack">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">Node.js</span>
                        <span class="tech-tag">MongoDB</span>
                    </div>
                    <a href="#" class="project-link">View Demo →</a>
                </div>
                <!-- Add other projects -->
            </div>
        </section>

        <section class="section" id="skills">
            <h2 class="section-title">Technical Arsenal</h2>
            <div class="skills-grid">
                <div class="skill-item">
                    <i class="fab fa-python"></i>
                    <h3>Python & Flask</h3>
                    <p>Backend Development, REST APIs</p>
                </div>
                <div class="skill-item">
                    <i class="fab fa-js"></i>
                    <h3>JavaScript</h3>
                    <p>Frontend Development, React</p>
                </div>
                <!-- Add other skills -->
            </div>
        </section>
    </main>

    <script>
        // Intersection Observer for scroll animations
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.section').forEach(section => {
            observer.observe(section);
        });

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Dynamic year update
        document.querySelector('#copyright-year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
