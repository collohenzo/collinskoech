
<template>
    <div>

    <nav class="navbar">
        <div class="logo">Dev<span>Portfolio</span></div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="home" class="hero-section">
        <div class="hero-content">
            <h1>Hi, I'm <span class="highlight">John Doe</span></h1>
            <h2>I am a <span id="dynamic-text"></span><span class="cursor">|</span></h2>
            <p>Crafting clean, responsive, and user-friendly web experiences.</p>
            <a href="#projects" class="btn">View My Work</a>
        </div>
    </section>

    <section id="about" class="about-section">
        <h2>About Me</h2>
        <div class="about-container">
            <div class="about-text">
                <p>Hello! I'm a passionate web developer focused on building modern web applications. I love solving complex problems and turning ideas into digital reality.</p>
                <div class="skills">
                    <span class="skill-badge">HTML5</span>
                    <span class="skill-badge">CSS3</span>
                    <span class="skill-badge">JavaScript</span>
                    <span class="skill-badge">Responsive Design</span>
                </div>
            </div>
        </div>
    </section>

    <section id="projects" class="projects-section">
        <h2>My Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <h3>Project One</h3>
                <p>A brief description of this amazing project and the tech stack used to build it.</p>
                <a href="#" class="project-link">view project</a>
            </div>
            <div class="project-card">
                <h3>Project Two</h3>
                <p>A brief description of this amazing project and the tech stack used to build it.</p>
                <a href="#" class="project-link">View Project <i class="fas fa-arrow-right"></i></a>
            </div>
            <div class="project-card">
                <h3>Project Three</h3>
                <p>A brief description of this amazing project and the tech stack used to build it.</p>
                <a href="#" class="project-link">View Project <i class="fas fa-arrow-right"></i></a>
            </div>
        </div>
    </section>

    <section id="contact" class="contact-section">
        <h2>Get In Touch</h2>
        <p>Have a project in mind or just want to say hi?</p>
        <a href="mailto:your.email@example.com" class="btn">Email Me</a>
        <div class="social-icons">
            <a href="#"><i class="fab fa-github"></i></a>
            <a href="#"><i class="fab fa-linkedin"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
        </div>
    </section>

    <footer>
        <p>&copy; 2026 DevPortfolio. All rights reserved.</p>
    </footer>
</div>
</template>
<style scoped>
/* Reset & Base Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    scroll-behavior: smooth;
}

:root {
    --bg-color: #0f172a;
    --card-bg: #1e293b;
    --text-color: #f8fafc;
    --text-muted: #94a3b8;
    --primary-color: #38bdf8;
    --primary-hover: #0ea5e9;
}

body {
    background-color: var(--bg-color);
    color: var(--text-color);
    line-height: 1.6;
}

section {
    padding: 100px 10%;
}

/* Navbar */
.navbar {
    position: fixed;
    top: 0;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 10%;
    background-color: rgba(15, 23, 42, 0.9);
    backdrop-filter: blur(10px);
    z-index: 1000;
}

.logo {
    font-size: 1.5rem;
    font-weight: 700;
}

.logo span {
    color: var(--primary-color);
}

.nav-links {
    display: flex;
    list-style: none;
}

.nav-links li {
    margin-left: 30px;
}

.nav-links a {
    color: var(--text-color);
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s;
}

.nav-links a:hover {
    color: var(--primary-color);
}

/* Hero Section */
.hero-section {
    height: 100vh;
    display: flex;
    align-items: center;
}

.hero-content h1 {
    font-size: 3.5rem;
    margin-bottom: 10px;
}

.hero-content h2 {
    font-size: 2rem;
    color: var(--text-muted);
    margin-bottom: 20px;
}

.highlight {
    color: var(--primary-color);
}

.btn {
    display: inline-block;
    padding: 12px 30px;
    background-color: var(--primary-color);
    color: var(--bg-color);
    font-weight: 600;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s, transform 0.2s;
}

.btn:hover {
    background-color: var(--primary-hover);
    transform: translateY(-2px);
}

/* About Section */
.about-section h2, .projects-section h2, .contact-section h2 {
    font-size: 2.5rem;
    margin-bottom: 30px;
    text-align: center;
}

.about-container {
    max-width: 800px;
    margin: 0 auto;
    text-align: center;
}

.skills {
    margin-top: 30px;
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
}

.skill-badge {
    background-color: var(--card-bg);
    padding: 8px 20px;
    border-radius: 20px;
    font-size: 0.9rem;
    border: 1px solid rgba(56, 189, 248, 0.2);
}

/* Projects Section */
.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 30px;
}

.project-card {
    background-color: var(--card-bg);
    padding: 30px;
    border-radius: 8px;
    transition: transform 0.3s;
    border: 1px solid transparent;
}

.project-card:hover {
    transform: translateY(-5px);
    border-color: rgba(56, 189, 248, 0.3);
}

.project-card h3 {
    margin-bottom: 15px;
}

.project-card p {
    color: var(--text-muted);
    font-size: 0.95rem;
    margin-bottom: 20px;
}

.project-link {
    color: var(--primary-color);
    text-decoration: none;
    font-weight: 500;
}

/* Contact Section */
.contact-section {
    text-align: center;
}

.contact-section p {
    color: var(--text-muted);
    margin-bottom: 30px;
}

.social-icons {
    margin-top: 40px;
}

.social-icons a {
    color: var(--text-color);
    font-size: 1.8rem;
    margin: 0 15px;
    transition: color 0.3s;
}

.social-icons a:hover {
    color: var(--primary-color);
}

/* Footer */
footer {
    text-align: center;
    padding: 20px;
    background-color: #0b111e;
    color: var(--text-muted);
    font-size: 0.9rem;
}

/* Typing Cursor Animation */
.cursor {
    animation: blink 0.7s infinite;
    color: var(--primary-color);
}

@keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
}

/* Responsive Design */
@media (max-width: 768px) {
    .navbar { padding: 20px 5%; }
    section { padding: 80px 5%; }
    .hero-content h1 { font-size: 2.5rem; }
mk    .nav-links { display: none; } /* Standard for keeping simple, can be expanded to hamburger menu */
}
</style>
