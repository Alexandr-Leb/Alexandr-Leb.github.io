<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alexandr Lebedyev | Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* General Styles */
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Roboto', sans-serif; }
        body { line-height: 1.6; color: #333; background-color: #f4f4f4; }

        /* Navigation */
        header { background: #111; color: #fff; padding: 1rem 0; position: sticky; top: 0; z-index: 1000; }
        nav { display: flex; justify-content: space-between; align-items: center; width: 90%; margin: auto; }
        nav .logo { font-weight: bold; font-size: 1.5rem; }
        nav ul { list-style: none; display: flex; }
        nav ul li { margin-left: 2rem; }
        nav ul li a { color: #fff; text-decoration: none; font-weight: 500; transition: color 0.3s; }
        nav ul li a:hover { color: #f39c12; }

        /* Hero Section */
        #hero {
            background: url('hero-bg.jpg') no-repeat center center/cover;
            height: 100vh; display: flex; justify-content: center; align-items: center; text-align: center; color: #fff;
        }
        #hero h1 { font-size: 3rem; margin-bottom: 1rem; }
        #hero p { font-size: 1.5rem; margin-bottom: 2rem; }

        /* Button */
        .btn {
            display: inline-block; padding: 0.75rem 2rem; background: #f39c12; color: #fff; border-radius: 5px; text-decoration: none; font-weight: 700; transition: background 0.3s;
        }
        .btn:hover { background: #e67e22; }

        /* Sections */
        section { padding: 4rem 2rem; text-align: center; }
        section h2 { font-size: 2.5rem; margin-bottom: 1.5rem; }

        /* Projects */
        .projects-container { display: flex; flex-wrap: wrap; justify-content: center; gap: 2rem; }
        .project-card {
            background: #fff; border-radius: 10px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); width: 300px; overflow: hidden; transition: transform 0.3s;
        }
        .project-card img { width: 100%; height: 200px; object-fit: cover; }
        .project-card h3 { margin: 1rem 0 0.5rem 0; }
        .project-card p { padding: 0 1rem 1rem 1rem; font-size: 0.95rem; }
        .project-card:hover { transform: translateY(-10px); }

        /* Contact */
        #contact a { color: #f39c12; text-decoration: none; }
        #contact a:hover { text-decoration: underline; }

        /* Footer */
        footer { background: #111; color: #fff; padding: 1rem 0; text-align: center; }

        /* Responsive */
        @media(max-width: 768px) {
            .projects-container { flex-direction: column; align-items: center; }
            nav ul { flex-direction: column; background: #111; position: absolute; top: 60px; right: -100%; width: 200px; transition: right 0.3s; }
            nav ul.active { right: 0; }
            nav ul li { margin: 1rem 0; }
            .menu-toggle { display: block; cursor: pointer; font-size: 1.5rem; color: #fff; }
        }
        .menu-toggle { display: none; }
    </style>
</head>
<body>

    <!-- Navigation -->
    <header>
        <nav>
            <div class="logo">AL</div>
            <div class="menu-toggle">&#9776;</div>
            <ul class="nav-links">
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="hero">
        <div class="hero-content">
            <h1>Hi, I'm Alexandr Lebedyev</h1>
            <p>Engineering Physics Student | Robotics & Software Developer</p>
            <a href="#projects" class="btn">View My Work</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2>About Me</h2>
        <p>
            I'm a UBC Engineering Physics student passionate about robotics, software development, and mechanical design. I love turning ideas into functional projects and learning by doing.
        </p>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2>Projects</h2>
        <div class="projects-container">
            <div class="project-card">
                <img src="project1.jpg" alt="Project 1">
                <h3>Autonomous Claw Project</h3>
                <p>Developed a robotic claw with autonomous navigation for object retrieval using sensors and actuators.</p>
                <a href="#" class="btn">View Details</a>
            </div>
            <div class="project-card">
                <img src="project2.jpg" alt="Project 2">
                <h3>Rescue Robot</h3>
                <p>Designed and built an autonomous robot capable of navigating obstacles and performing rescue tasks.</p>
                <a href="#" class="btn">View Details</a>
            </div>
            <div class="project-card">
                <img src="project3.jpg" alt="Project 3">
                <h3>Solar Microgrid Design</h3>
                <p>Engineered a solar microgrid system with battery storage for remote communities.</p>
                <a href="#" class="btn">View Details</a>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact Me</h2>
        <p>Email: <a href="mailto:lebedyevalexandr@gmail.com">lebedyevalexandr@gmail.com</a></p>
        <p>Phone: 604.722.9535</p>
        <p>Feel free to reach out for collaborations or inquiries!</p>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 Alexandr Lebedyev. All rights reserved.</p>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Mobile menu toggle
        const menuToggle = document.querySelector('.menu-toggle');
        const navLinks = document.querySelector('.nav-links');
        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
    </script>
</body>
</html>
