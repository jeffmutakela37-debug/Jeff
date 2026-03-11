
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jeff MTK | MediaGraphix</title>
    <style>
        /* --- RESET & BASIC STYLES --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            background-color: #0f0f0f;
            color: #f0f0f0;
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
            transition: 0.3s;
        }

        ul {
            list-style: none;
        }

        /* --- TYPOGRAPHY --- */
        h1, h2, h3 {
            font-weight: 700;
            letter-spacing: -1px;
        }

        .highlight {
            color: #00d4ff; /* Electric Blue Accent */
        }

        /* --- NAVIGATION --- */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 5%;
            position: fixed;
            width: 100%;
            top: 0;            background: rgba(15, 15, 15, 0.95);
            z-index: 1000;
            border-bottom: 1px solid #333;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a:hover {
            color: #00d4ff;
        }

        .btn-cta {
            padding: 10px 25px;
            background-color: #00d4ff;
            color: #000;
            font-weight: bold;
            border-radius: 50px;
        }

        .btn-cta:hover {
            background-color: #fff;
        }

        /* --- HERO SECTION --- */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 120px 5% 80px;
            background: linear-gradient(135deg, #0f0f0f 0%, #1a1a1a 100%);
        }

        .hero-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
            max-width: 1400px;
            margin: 0 auto;
        }

        .hero-content h1 {            font-size: 3.5rem;
            margin-bottom: 20px;
            line-height: 1.1;
        }

        .hero-content p {
            font-size: 1.2rem;
            color: #aaa;
            margin-bottom: 30px;
        }

        .hero-image {
            position: relative;
        }

        .hero-image img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 20px 60px rgba(0, 212, 255, 0.2);
        }

        /* --- ABOUT SECTION --- */
        .section {
            padding: 100px 5%;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
            max-width: 1400px;
            margin: 0 auto;
        }

        .about-images {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .about-images img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 10px;
            border: 2px solid #333;
        }
        .about-text h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .about-text p {
            margin-bottom: 20px;
            color: #ccc;
        }

        /* --- GALLERY SECTION --- */
        .gallery {
            background-color: #141414;
        }

        .gallery h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .gallery-subtitle {
            text-align: center;
            color: #aaa;
            margin-bottom: 60px;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            max-width: 1400px;
            margin: 0 auto;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            border: 2px solid #333;
            transition: transform 0.3s, border-color 0.3s;
        }

        .gallery-item:hover {
            transform: translateY(-10px);
            border-color: #00d4ff;
        }

        .gallery-item img {
            width: 100%;            height: 400px;
            object-fit: cover;
            display: block;
        }

        .gallery-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0, 0, 0, 0.9), transparent);
            padding: 30px;
            transform: translateY(100%);
            transition: transform 0.3s;
        }

        .gallery-item:hover .gallery-overlay {
            transform: translateY(0);
        }

        .gallery-overlay h3 {
            color: #00d4ff;
            font-size: 1.3rem;
        }

        /* --- SERVICES SECTION --- */
        .services h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 60px;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            max-width: 1400px;
            margin: 0 auto;
        }

        .service-card {
            background: #1f1f1f;
            padding: 40px;
            border-radius: 8px;
            border: 1px solid #333;
            transition: transform 0.3s;
        }

        .service-card:hover {
            transform: translateY(-10px);            border-color: #00d4ff;
        }

        .service-card h3 {
            margin-bottom: 15px;
            font-size: 1.5rem;
        }

        .service-card p {
            color: #aaa;
            font-size: 0.95rem;
        }

        /* --- CONTACT SECTION --- */
        .contact {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        .contact h2 {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .contact p {
            margin-bottom: 40px;
            color: #aaa;
        }

        form {
            max-width: 500px;
            margin: 0 auto;
            text-align: left;
        }

        input, textarea {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            background: #1f1f1f;
            border: 1px solid #333;
            color: #fff;
            border-radius: 5px;
            font-family: inherit;
        }

        input:focus, textarea:focus {
            outline: none;
            border-color: #00d4ff;        }

        button[type="submit"] {
            width: 100%;
            padding: 15px;
            background: #00d4ff;
            border: none;
            color: #000;
            font-weight: bold;
            font-size: 1rem;
            cursor: pointer;
            border-radius: 5px;
        }

        /* --- FOOTER --- */
        footer {
            padding: 40px;
            text-align: center;
            border-top: 1px solid #333;
            color: #666;
            font-size: 0.9rem;
        }

        /* --- MOBILE RESPONSIVE --- */
        @media (max-width: 968px) {
            .hero-container,
            .about-grid {
                grid-template-columns: 1fr;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .about-images {
                grid-template-columns: 1fr;
            }

            .nav-links {
                display: none;
            }
        }
    </style>
</head>
<body>

    <!-- NAVIGATION -->
    <nav>
        <div class="logo">Jeff MTK <span class="highlight">| MediaGraphix</span></div>
        <div class="nav-links">            <a href="#about">About</a>
            <a href="#gallery">Gallery</a>
            <a href="#services">Services</a>
            <a href="#contact" class="btn-cta">Start a Project</a>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <section class="hero">
        <div class="hero-container">
            <div class="hero-content">
                <h1>Where Data Meets <br><span class="highlight">Design.</span></h1>
                <p>MediaGraphix is the creative studio led by Jeff MTK. We transform complex ideas into visual masterpieces that drive engagement and elevate brands.</p>
                <a href="#contact" class="btn-cta">Let's Work Together</a>
            </div>
            <div class="hero-image">
                <!-- Replace with Image 1: Professional pose with hand on chin -->
                <img src="jeff-mtk-hero.jpg" alt="Jeff MTK - Founder of MediaGraphix">
            </div>
        </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="about" class="section">
        <div class="about-grid">
            <div class="about-images">
                <!-- Replace with Image 2: In front of modern building -->
                <img src="jeff-mtk-about-1.jpg" alt="Jeff MTK Professional">
                <!-- Replace with Image 3: Two-tone suit -->
                <img src="jeff-mtk-about-2.jpg" alt="Jeff MTK Creative Director">
            </div>
            <div class="about-text">
                <h2>The Vision of <span class="highlight">Jeff MTK</span></h2>
                <p>In a world saturated with noise, clarity is king. MediaGraphix was founded on the principle that good design isn't just about aesthetics—it's about communication.</p>
                <p>Led by Jeff MTK, we bridge the gap between technical media strategy and high-end graphic artistry. Whether you are a startup needing a brand identity or a corporation looking for a digital overhaul, we bring a unique perspective that combines logic with creativity.</p>
                <a href="#contact" class="btn-cta">Get In Touch</a>
            </div>
        </div>
    </section>

    <!-- GALLERY SECTION -->
    <section id="gallery" class="section gallery">
        <h2>Behind The Scenes</h2>
        <p class="gallery-subtitle">A glimpse into the creative process</p>
        <div class="gallery-grid">
            <div class="gallery-item">
                <!-- Replace with Image 4: In front of building with windows -->
                <img src="jeff-mtk-gallery-1.jpg" alt="MediaGraphix Workspace">
                <div class="gallery-overlay">
                    <h3>Creative Strategy</h3>                </div>
            </div>
            <div class="gallery-item">
                <!-- Replace with Image 5: Same as image 2 or alternate -->
                <img src="jeff-mtk-gallery-2.jpg" alt="MediaGraphix Projects">
                <div class="gallery-overlay">
                    <h3>Brand Development</h3>
                </div>
            </div>
            <div class="gallery-item">
                <!-- You can add another image or repeat one -->
                <img src="jeff-mtk-gallery-3.jpg" alt="MediaGraphix Team">
                <div class="gallery-overlay">
                    <h3>Digital Innovation</h3>
                </div>
            </div>
        </div>
    </section>

    <!-- SERVICES SECTION -->
    <section id="services" class="section services">
        <h2>Our Expertise</h2>
        <div class="services-grid">
            <div class="service-card">
                <h3>Brand Identity</h3>
                <p>More than just a logo. We build comprehensive visual systems that tell your company's story and resonate with your audience.</p>
            </div>
            <div class="service-card">
                <h3>Digital Media</h3>
                <p>Web design, UI/UX, and interactive experiences. We create digital environments that are intuitive, fast, and beautiful.</p>
            </div>
            <div class="service-card">
                <h3>Motion Graphics</h3>
                <p>Static images are great, but motion captures attention. We specialize in animation for social media, web, and broadcast.</p>
            </div>
            <div class="service-card">
                <h3>Strategy</h3>
                <p>Design without direction is just art. We provide the strategic roadmap to ensure your visuals hit your business goals.</p>
            </div>
        </div>
    </section>

    <!-- CONTACT SECTION -->
    <section id="contact" class="section contact">
        <h2>Ready to Create?</h2>
        <p>Tell Jeff MTK and the MediaGraphix team about your next big idea.</p>
        
        <form>
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>            <textarea rows="5" placeholder="Tell us about your project..." required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <!-- FOOTER -->
    <footer>
        <p>&copy; 2026 MediaGraphix. All Rights Reserved. Designed by Jeff MTK.</p>
    </footer>

</body>
</html>