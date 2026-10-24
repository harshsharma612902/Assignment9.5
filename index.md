The Updated HTML File (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NexusCloud — Portfolio-Ready Landing Page</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- ================= HEADER & NAVIGATION ================= -->
    <header class="site-header">
        <div class="nav-container">
            <a href="#" class="logo">NexusCloud</a>
            
            <!-- Mobile Menu Toggle Button -->
            <button class="menu-toggle" aria-label="Toggle navigation menu">
                <span></span>
                <span></span>
                <span></span>
            </button>

            <!-- Navigation Links -->
            <nav class="nav-links">
                <a href="#features">Features</a>
                <a href="#solutions">Solutions</a>
                <a href="#pricing">Pricing</a>
                <a href="#about">About</a>
                <div class="mobile-actions">
                    <a href="#signup" class="btn btn-secondary w-full">Sign In</a>
                    <a href="#get-started" class="btn btn-primary w-full">Get Started</a>
                </div>
            </nav>

            <!-- Desktop Actions -->
            <div class="nav-action desktop-only">
                <a href="#signup" class="btn btn-secondary">Sign In</a>
                <a href="#get-started" class="btn btn-primary">Get Started</a>
            </div>
        </div>
    </header>

    <main>
        <!-- ================= HERO SECTION ================= -->
        <section class="hero-section">
            <div class="hero-container">
                <div class="hero-content">
                    <span class="badge">Version 3.0 Released</span>
                    <h1>Cloud Infrastructure Made Effortless</h1>
                    <p>Deploy, scale, and secure your applications globally with automated workflows and enterprise-grade reliability designed for modern engineering teams.</p>
                    <div class="hero-buttons">
                        <a href="#start" class="btn btn-primary btn-lg">Start Free Trial</a>
                        <a href="#demo" class="btn btn-outline btn-lg">Watch Overview</a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&q=80&w=600" alt="Cloud Dashboard Interface">
                </div>
            </div>
        </section>

        <!-- ================= FEATURE CARDS SECTION ================= -->
        <section id="features" class="features-section">
            <div class="section-container">
                <div class="section-title">
                    <h2>Engineered for High Performance</h2>
                    <p>Everything you need to run production workloads with total confidence.</p>
                </div>

                <div class="features-grid">
                    <!-- Card 1 -->
                    <article class="feature-card">
                        <div class="card-icon">⚡</div>
                        <h3>Global Edge Network</h3>
                        <p>Deliver ultra-low latency experiences to your users via our distributed CDN infrastructure.</p>
                    </article>

                    <!-- Card 2 -->
                    <article class="feature-card">
                        <div class="card-icon">🔒</div>
                        <h3>Advanced Security</h3>
                        <p>Automated SSL certificates, DDoS mitigation, and continuous vulnerability scanning included.</p>
                    </article>

                    <!-- Card 3 -->
                    <article class="feature-card">
                        <div class="card-icon">📈</div>
                        <h3>Real-Time Analytics</h3>
                        <p>Gain deep operational insights with custom metrics, instant alerts, and log streaming.</p>
                    </article>
                </div>
            </div>
        </section>
    </main>

    <!-- ================= FOOTER ================= -->
    <footer class="site-footer">
        <div class="footer-container">
            <p>&copy; 2026 NexusCloud Inc. All rights reserved.</p>
            <div class="footer-links">
                <a href="#privacy">Privacy Policy</a>
                <a href="#terms">Terms of Service</a>
                <a href="#security">Security</a>
            </div>
        </div>
    </footer>

</body>
</html>
2. The Updated CSS File (style.css)
CSS
/* ==========================================================================
   Design Tokens & Global Reset
   ========================================================================== */
:root {
    --primary-blue: #2563eb;
    --primary-hover: #1d4ed8;
    --dark-slate: #0f172a;
    --text-main: #1e293b;
    --text-muted: #64748b;
    --bg-page: #f8fafc;
    --bg-card: #ffffff;
    --border-color: #e2e8f0;

    --radius-sm: 6px;
    --radius-md: 10px;
    --radius-full: 9999px;

    --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.05);
    --shadow-md: 0 10px 15px -3px rgba(0, 0, 0, 0.05), 0 4px 6px -2px rgba(0, 0, 0, 0.025);
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
    background-color: var(--bg-page);
    color: var(--text-main);
    line-height: 1.6;
    overflow-x: hidden; /* Step 6: Prevents unwanted horizontal scroll */
}

/* ==========================================================================
   Header & Navigation (Flexbox Layout)
   ========================================================================== */
.site-header {
    background-color: var(--bg-card);
    border-bottom: 1px solid var(--border-color);
    position: sticky;
    top: 0;
    z-index: 1000;
    box-shadow: var(--shadow-sm);
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 16px 24px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-size: 1.4rem;
    font-weight: 800;
    color: var(--primary-blue);
    text-decoration: none;
    letter-spacing: -0.5px;
}

.nav-links {
    display: flex;
    gap: 32px;
    align-items: center;
}

.nav-links a:not(.btn) {
    text-decoration: none;
    color: var(--text-muted);
    font-weight: 600;
    font-size: 0.95rem;
    transition: color 0.2s;
}

.nav-links a:not(.btn):hover {
    color: var(--primary-blue);
}

.nav-action {
    display: flex;
    gap: 12px;
    align-items: center;
}

.menu-toggle {
    display: none; /* Hidden on desktop */
    background: none;
    border: none;
    cursor: pointer;
    flex-direction: column;
    gap: 5px;
    padding: 4px;
}

.menu-toggle span {
    display: block;
    width: 24px;
    height: 2px;
    background-color: var(--dark-slate);
    transition: 0.3s;
}

.mobile-actions {
    display: none; /* Hidden on desktop */
}

/* ==========================================================================
   Buttons
   ========================================================================== */
.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 10px 20px;
    border-radius: var(--radius-sm);
    font-weight: 600;
    font-size: 0.95rem;
    text-decoration: none;
    cursor: pointer;
    transition: background-color 0.2s, transform 0.1s;
}

.btn:active {
    transform: scale(0.98);
}

.btn-lg {
    padding: 14px 28px;
    font-size: 1.05rem;
}

.btn-primary {
    background-color: var(--primary-blue);
    color: #ffffff;
}

.btn-primary:hover {
    background-color: var(--primary-hover);
}

.btn-secondary {
    background-color: transparent;
    color: var(--text-main);
}

.btn-secondary:hover {
    background-color: #f1f5f9;
}

.btn-outline {
    background-color: transparent;
    color: var(--text-main);
    border: 1px solid var(--border-color);
}

.btn-outline:hover {
    background-color: #f1f5f9;
}

.w-full {
    width: 100%;
}

/* ==========================================================================
   Hero Section (Flexbox Layout)
   ========================================================================== */
.hero-section {
    padding: 80px 24px;
}

.hero-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 60px;
}

.hero-content {
    flex: 1;
    max-width: 580px;
}

.badge {
    display: inline-block;
    background-color: #dbeafe;
    color: var(--primary-blue);
    font-size: 0.8rem;
    font-weight: 700;
    padding: 4px 12px;
    border-radius: var(--radius-full);
    text-transform: uppercase;
    margin-bottom: 20px;
    letter-spacing: 0.5px;
}

.hero-content h1 {
    font-size: clamp(2rem, 3.5vw + 1rem, 3rem); /* Fluid typography */
    font-weight: 800;
    color: var(--dark-slate);
    line-height: 1.15;
    margin-bottom: 20px;
    letter-spacing: -1px;
}

.hero-content p {
    font-size: 1.1rem;
    color: var(--text-muted);
    margin-bottom: 32px;
}

.hero-buttons {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
}

.hero-image {
    flex: 1;
    text-align: right;
}

.hero-image img {
    width: 100%;
    max-width: 560px;
    height: auto; /* Responsive image constraint */
    border-radius: var(--radius-md);
    box-shadow: var(--shadow-md);
}

/* ==========================================================================
   Feature Cards Section (CSS Grid Layout)
   ========================================================================== */
.features-section {
    padding: 80px 24px;
    background-color: var(--bg-card);
    border-top: 1px solid var(--border-color);
    border-bottom: 1px solid var(--border-color);
}

.section-container {
    max-width: 1200px;
    margin: 0 auto;
}

.section-title {
    text-align: center;
    max-width: 600px;
    margin: 0 auto 50px auto;
}

.section-title h2 {
    font-size: clamp(1.75rem, 2.5vw + 1rem, 2.25rem);
    color: var(--dark-slate);
    margin-bottom: 10px;
}

.section-title p {
    color: var(--text-muted);
    font-size: 1.05rem;
}

.features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 30px;
}

.feature-card {
    background-color: var(--bg-page);
    border: 1px solid var(--border-color);
    border-radius: var(--radius-md);
    padding: 32px;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.feature-card:hover {
    transform: translateY(-4px);
    box-shadow: var(--shadow-md);
}

.card-icon {
    font-size: 2.25rem;
    margin-bottom: 16px;
}

.feature-card h3 {
    font-size: 1.25rem;
    color: var(--dark-slate);
    margin-bottom: 8px;
}

.feature-card p {
    color: var(--text-muted);
    font-size: 0.95rem;
}

/* ==========================================================================
   Footer
   ========================================================================== */
.site-footer {
    background-color: var(--bg-card);
    padding: 32px 24px;
}

.footer-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 16px;
    font-size: 0.875rem;
    color: var(--text-muted);
}

.footer-links {
    display: flex;
    gap: 24px;
}

.footer-links a {
    text-decoration: none;
    color: var(--text-muted);
    transition: color 0.2s;
}

.footer-links a:hover {
    color: var(--primary-blue);
}


/* ==========================================================================
   Steps 1, 2, & 5: Tablet & Mobile Breakpoints
   ========================================================================== */

/* Tablet View (max-width: 1024px) */
@media (max-width: 1024px) {
    .hero-container {
        gap: 40px;
    }
}

/* Mobile View (max-width: 768px) */
@media (max-width: 768px) {
    /* Navbar adjustments */
    .desktop-only {
        display: none;
    }

    .menu-toggle {
        display: flex;
    }

    .nav-links {
        display: none; /* In production, toggled via JS; kept hidden or vertical here */
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background-color: var(--bg-card);
        flex-direction: column;
        align-items: flex-start;
        padding: 24px;
        border-bottom: 1px solid var(--border-color);
        box-shadow: var(--shadow-md);
        gap: 16px;
    }

    /* Note: To make toggle functional without JS in static CSS demo, 
       developers usually hook up a checkbox hack or JS listener. 
       Here we make mobile-actions visible inside nav when active or stacked */
    .mobile-actions {
        display: flex;
        flex-direction: column;
        width: 100%;
        gap: 12px;
        margin-top: 12px;
    }

    /* Hero adjustments */
    .hero-section {
        padding: 48px 16px;
    }

    .hero-container {
        flex-direction: column;
        text-align: center;
        gap: 40px;
    }

    .hero-content {
        max-width: 100%;
    }

    .hero-buttons {
        justify-content: center;
    }

    .hero-image {
        text-align: center;
    }

    /* Features adjustments */
    .features-section {
        padding: 48px 16px;
    }

    .features-grid {
        grid-template-columns: 1fr;
    }

    /* Footer adjustments */
    .footer-container {
        flex-direction: column;
        text-align: center;
        gap: 16px;
    }
}