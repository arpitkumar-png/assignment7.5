HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tech Innovators Club — Responsive Landing Page</title>
    <!-- Link to External Stylesheet -->
    <link rel="stylesheet" href="landing-style.css">
</head>
<body>

    <!-- --- 1. NAVIGATION BAR --- -->
    <header class="site-header">
        <nav class="navbar">
            <div class="nav-logo">
                <a href="#">Tech Innovators</a>
            </div>
            <ul class="nav-links">
                <li><a href="#hero">Home</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="#cta">Join</a></li>
            </ul>
            <div class="nav-cta">
                <a href="#cta" class="btn-primary">Get Started</a>
            </div>
        </nav>
    </header>

    <main>
        <!-- --- 2. HERO SECTION (Side-by-side Flexbox) --- -->
        <section id="hero" class="hero-section">
            <div class="hero-container">
                <div class="hero-text">
                    <span class="hero-badge">Welcome to 2026</span>
                    <h1>Empowering Future Tech Leaders</h1>
                    <p>Join a collaborative community of student developers, designers, and creators building real-world projects and mastering modern web development.</p>
                    <div class="hero-buttons">
                        <a href="#cta" class="btn-primary btn-large">Become a Member</a>
                        <a href="#features" class="btn-secondary btn-large">Explore Features</a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?w=600&auto=format&fit=crop&q=80" alt="Students collaborating on laptops">
                </div>
            </div>
        </section>

        <!-- --- 3. THREE FEATURE CARDS SECTION (Responsive Row) --- -->
        <section id="features" class="features-section">
            <div class="features-container">
                <h2>Why Join Our Club?</h2>
                <p class="section-desc">Discover the core benefits of becoming an active member of our technical community.</p>
                
                <div class="cards-wrapper">
                    <!-- Feature Card 1 -->
                    <article class="feature-card">
                        <div class="card-icon">⚡</div>
                        <h3>Hands-On Workshops</h3>
                        <p>Participate in weekly coding sessions covering HTML, CSS, JavaScript, Git, and full-stack architecture.</p>
                    </article>

                    <!-- Feature Card 2 -->
                    <article class="feature-card">
                        <div class="card-icon">🤝</div>
                        <h3>Peer Collaboration</h3>
                        <p>Work in teams on open-source projects, hackathons, and real client applications to build your portfolio.</p>
                    </article>

                    <!-- Feature Card 3 -->
                    <article class="feature-card">
                        <div class="card-icon">🚀</div>
                        <h3>Industry Networking</h3>
                        <p>Connect with alumni, guest speakers, and tech recruiters looking for driven student developers.</p>
                    </article>
                </div>
            </div>
        </section>

        <!-- --- 4. CALL-TO-ACTION SECTION --- -->
        <section id="cta" class="cta-section">
            <div class="cta-container">
                <h2>Ready to Start Your Tech Journey?</h2>
                <p>Membership is open to all university students regardless of major or experience level.</p>
                <a href="registration.html" class="btn-light btn-large">Register for Membership</a>
            </div>
        </section>
    </main>

    <!-- --- 5. FOOTER --- -->
    <footer class="site-footer">
        <div class="footer-container">
            <p>&copy; 2026 Tech Innovators Club. All rights reserved.</p>
            <ul class="footer-links">
                <li><a href="#">Privacy Policy</a></li>
                <li><a href="#">Terms of Service</a></li>
                <li><a href="#">Contact Us</a></li>
            </ul>
        </div>
    </footer>

</body>
</html>
File 2: landing-style.css (Stylesheet)
CSS
/* --- Global Reset & Design Tokens --- */
:root {
    --primary-color: #1e3a8a;       /* Deep Navy */
    --secondary-color: #2563eb;     /* Vibrant Blue */
    --accent-color: #38bdf8;        /* Sky Blue */
    --bg-light: #f8fafc;            /* Light Background */
    --card-bg: #ffffff;             /* White Containers */
    --text-main: #1e293b;           /* Dark Slate Text */
    --text-muted: #64748b;          /* Muted Gray Text */
    --border-color: #e2e8f0;        /* Subtle Border */
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    scroll-behavior: smooth;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: var(--bg-light);
    color: var(--text-main);
    line-height: 1.6;
}

/* ==========================================
   1. NAVIGATION BAR (Flexbox)
   ================================---------- */
.site-header {
    background-color: var(--card-bg);
    border-bottom: 1px solid var(--border-color);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.navbar {
    max-width: 1200px;
    margin: 0 auto;
    padding: 1rem 2rem;
    display: flex;                  /* Flexbox */
    justify-content: space-between;   /* Space items out */
    align-items: center;              /* Vertical alignment */
    flex-wrap: wrap;                  /* Wrap on small screens */
    gap: 1rem;
}

.nav-logo a {
    font-size: 1.3rem;
    font-weight: 700;
    color: var(--primary-color);
    text-decoration: none;
}

.nav-links {
    list-style: none;
    display: flex;
    gap: 2rem;
}

.nav-links a {
    text-decoration: none;
    color: var(--text-muted);
    font-weight: 500;
    transition: color 0.2s ease;
}

.nav-links a:hover {
    color: var(--secondary-color);
}

/* ==========================================
   2. HERO SECTION (Side-by-Side Flexbox)
   ================================---------- */
.hero-section {
    background: linear-gradient(135deg, #f8fafc 0%, #eff6ff 100%);
    padding: 5rem 1.5rem;
}

.hero-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;                  /* Side-by-side flexbox */
    align-items: center;            /* Vertical centering */
    justify-content: space-between;
    flex-wrap: wrap;                /* Wrap on mobile */
    gap: 3rem;
}

.hero-text {
    flex: 1 1 500px;
}

.hero-badge {
    display: inline-block;
    background-color: #dbeafe;
    color: #1e40af;
    font-size: 0.8rem;
    font-weight: 700;
    padding: 0.3rem 0.8rem;
    border-radius: 50px;
    text-transform: uppercase;
    margin-bottom: 1rem;
}

.hero-text h1 {
    font-size: 2.8rem;
    font-weight: 800;
    color: var(--primary-color);
    line-height: 1.2;
    margin-bottom: 1rem;
}

.hero-text p {
    font-size: 1.1rem;
    color: var(--text-muted);
    margin-bottom: 2rem;
}

.hero-buttons {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
}

.hero-image {
    flex: 1 1 450px;
    text-align: center;
}

.hero-image img {
    width: 100%;
    max-width: 500px;
    height: auto;
    border-radius: 12px;
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
}

/* ==========================================
   3. THREE FEATURE CARDS SECTION (Responsive Row)
   ================================---------- */
.features-section {
    padding: 5rem 1.5rem;
    background-color: var(--card-bg);
}

.features-container {
    max-width: 1200px;
    margin: 0 auto;
    text-align: center;
}

.features-container h2 {
    font-size: 2rem;
    color: var(--primary-color);
    margin-bottom: 0.5rem;
}

.section-desc {
    color: var(--text-muted);
    margin-bottom: 3rem;
}

/* Flexbox Cards Wrapper */
.cards-wrapper {
    display: flex;                  /* Flexbox row */
    flex-wrap: wrap;                /* Wrap cards on smaller screens */
    justify-content: center;        /* Center cards */
    align-items: stretch;           /* Equal height cards */
    gap: 2rem;                      /* Spacing between cards */
}

.feature-card {
    background-color: var(--bg-light);
    border: 1px solid var(--border-color);
    border-radius: 12px;
    padding: 2.5rem 2rem;
    flex: 1 1 300px;                /* Responsive grow, shrink, basis */
    max-width: 360px;
    text-align: left;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.feature-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.05);
}

.card-icon {
    font-size: 2.2rem;
    margin-bottom: 1rem;
}

.feature-card h3 {
    font-size: 1.25rem;
    color: var(--primary-color);
    margin-bottom: 0.75rem;
}

.feature-card p {
    font-size: 0.95rem;
    color: var(--text-muted);
}

/* ==========================================
   4. CALL-TO-ACTION SECTION
   ================================---------- */
.cta-section {
    background: linear-gradient(135deg, var(--primary-color), #0f172a);
    color: #ffffff;
    padding: 5rem 1.5rem;
    text-align: center;
}

.cta-container {
    max-width: 800px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1.25rem;
}

.cta-container h2 {
    font-size: 2.2rem;
}

.cta-container p {
    color: #cbd5e1;
    font-size: 1.1rem;
    margin-bottom: 1rem;
}

/* ==========================================
   SHARED BUTTON STYLES
   ================================---------- */
.btn-primary {
    background-color: var(--secondary-color);
    color: #ffffff;
    font-weight: 600;
    text-decoration: none;
    padding: 0.6rem 1.25rem;
    border-radius: 6px;
    transition: background-color 0.2s ease;
    display: inline-block;
}

.btn-primary:hover {
    background-color: #1d4ed8;
}

.btn-secondary {
    background-color: #ffffff;
    color: var(--text-main);
    font-weight: 600;
    text-decoration: none;
    padding: 0.6rem 1.25rem;
    border: 1px solid var(--border-color);
    border-radius: 6px;
    transition: background-color 0.2s ease;
    display: inline-block;
}

.btn-secondary:hover {
    background-color: var(--bg-light);
}

.btn-light {
    background-color: #ffffff;
    color: var(--primary-color);
    font-weight: 600;
    text-decoration: none;
    padding: 0.8rem 2rem;
    border-radius: 6px;
    transition: background-color 0.2s ease;
    display: inline-block;
}

.btn-light:hover {
    background-color: #f1f5f9;
}

.btn-large {
    padding: 0.8rem 1.75rem;
    font-size: 1rem;
}

/* ==========================================
   5. FOOTER
   ================================---------- */
.site-footer {
    background-color: #0f172a;
    color: #94a3b8;
    padding: 2rem;
}

.footer-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-space-between;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 1.5rem;
    font-size: 0.9rem;
}

.footer-links {
    list-style: none;
    display: flex;
    gap: 1.5rem;
}

.footer-links a {
    color: #94a3b8;
    text-decoration: none;
    transition: color 0.2s ease;
}

.footer-links a:hover {
    color: #ffffff;
}