# winglash.github.io
MUA
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WingLash - Professional Makeup Academy</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --rose-gold: #E8B4A0;
            --deep-burgundy: #722F37;
            --champagne: #F7E7CE;
            --black: #1a1a1a;
            --white: #ffffff;
            --nude-pink: #D4A5A5;
            --bronze: #CD7F32;
            --pearl: #F8F6F0;
        }

        body {
            font-family: 'Georgia', serif;
            line-height: 1.6;
            color: var(--black);
            overflow-x: hidden;
        }

        /* Header */
        .header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(26, 26, 26, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .logo-main {
            height: 45px;
            width: auto;
            filter: brightness(1.2) contrast(1.1);
        }

        .logo-icon {
            width: 45px;
            height: 45px;
            background: linear-gradient(135deg, var(--rose-gold), var(--bronze));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(232, 180, 160, 0.3);
        }

        .logo-icon::before {
            content: 'WL';
            font-size: 20px;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            filter: sepia(100%) saturate(200%) hue-rotate(320deg);
        }

        .logo-text {
            color: var(--rose-gold);
            font-size: 1.8rem;
            font-weight: bold;
            letter-spacing: 2px;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            color: var(--rose-gold);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: var(--rose-gold);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, var(--deep-burgundy) 0%, var(--black) 100%);
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><defs><radialGradient id="grad" cx="50%" cy="50%" r="50%"><stop offset="0%" stop-color="%23E8B4A0" stop-opacity="0.1"/><stop offset="100%" stop-color="%23722F37" stop-opacity="0.05"/></radialGradient></defs><circle cx="200" cy="200" r="100" fill="url(%23grad)"/><circle cx="800" cy="300" r="150" fill="url(%23grad)"/><circle cx="600" cy="700" r="120" fill="url(%23grad)"/></svg>');
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .hero-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: grid;
            grid-template-columns: 1fr 1fr;
            align-items: center;
            gap: 4rem;
            z-index: 2;
            position: relative;
        }

        .hero-text h1 {
            font-size: 3.5rem;
            color: var(--white);
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .hero-text .highlight {
            color: var(--rose-gold);
            font-style: italic;
        }

        .hero-text p {
            font-size: 1.2rem;
            color: var(--champagne);
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(135deg, var(--rose-gold), var(--bronze));
            color: var(--white);
            padding: 1rem 2rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(232, 180, 160, 0.3);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(232, 180, 160, 0.4);
        }

        .hero-visual {
            position: relative;
            height: 500px;
        }

        .makeup-showcase {
            position: absolute;
            width: 300px;
            height: 400px;
            background: linear-gradient(145deg, var(--pearl), var(--champagne));
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.2);
            overflow: hidden;
            animation: showcase-float 6s ease-in-out infinite;
        }

        @keyframes showcase-float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-10px) rotate(2deg); }
        }

        .makeup-showcase::before {
            content: '';
            position: absolute;
            top: 20%;
            left: 20%;
            width: 60%;
            height: 30%;
            background: var(--rose-gold);
            border-radius: 50%;
            opacity: 0.7;
        }

        .makeup-showcase::after {
            content: '';
            position: absolute;
            bottom: 30%;
            right: 25%;
            width: 40%;
            height: 20%;
            background: var(--deep-burgundy);
            border-radius: 20px;
            opacity: 0.8;
        }

        /* About Section */
        .about {
            padding: 6rem 0;
            background: var(--pearl);
        }

        .about-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--deep-burgundy);
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: linear-gradient(to right, var(--rose-gold), var(--bronze));
        }

        .founders-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 3rem;
            margin-top: 4rem;
        }

        .founder-card {
            background: var(--white);
            border-radius: 20px;
            padding: 2rem;
            box-shadow: 0 15px 50px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
            border: 1px solid rgba(232, 180, 160, 0.2);
        }

        .founder-card:hover {
            transform: translateY(-10px);
        }

        .founder-avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 0 auto 1.5rem;
            background-size: cover;
            background-position: center;
            border: 4px solid var(--rose-gold);
            box-shadow: 0 10px 30px rgba(232, 180, 160, 0.3);
            transition: all 0.3s ease;
        }

        .founder-avatar.khushbu {
            background-image: url('data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAYEBQYFBAYGBQYHBwYIChAKCgkJChQODwwQFxQYGBcUFhYaHSUfGhsjHBYWICwgIyYnKSopGR8tMC0oMCUoKSj/2wBDAQcHBwoIChMKChMoGhYaKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCj/wAARCAC8AUIDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1+iiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigD//2Q==');
        }

        .founder-avatar.shruti {
            background-image: url('data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAYEBQYFBAYGBQYHBwYIChAKCgkJChQODwwQFxQYGBcUFhYaHSUfGhsjHBYWICwgIyYnKSopGR8tMC0oMCUoKSj/2wBDAQcHBwoIChMKChMoGhYaKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCj/wAARCADgAOADASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1+iiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigD//2Q==');
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 1rem;
        }

        .instagram-link {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: linear-gradient(135deg, #E1306C, #F56040);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            text-decoration: none;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(225, 48, 108, 0.3);
        }

        .instagram-link:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(225, 48, 108, 0.4);
        }

        .instagram-icon {
            width: 18px;
            height: 18px;
            fill: currentColor;
        }

        .founder-name {
            font-size: 1.5rem;
            color: var(--deep-burgundy);
            text-align: center;
            margin-bottom: 0.5rem;
        }

        .founder-title {
            color: var(--bronze);
            text-align: center;
            font-style: italic;
            margin-bottom: 1rem;
        }

        .founder-description {
            color: var(--black);
            opacity: 0.8;
            text-align: center;
            line-height: 1.6;
        }

        /* Courses Section */
        .courses {
            padding: 6rem 0;
            background: linear-gradient(135deg, var(--champagne) 0%, var(--pearl) 100%);
        }

        .courses-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 4rem;
        }

        .course-card {
            background: var(--white);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .course-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 30px 80px rgba(0,0,0,0.15);
        }

        .course-image {
            height: 200px;
            background: linear-gradient(135deg, var(--rose-gold), var(--bronze));
            position: relative;
            overflow: hidden;
        }

        .course-image::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 80px;
            height: 80px;
            background: var(--white);
            border-radius: 50%;
            opacity: 0.9;
        }

        .course-content {
            padding: 2rem;
        }

        .course-title {
            font-size: 1.3rem;
            color: var(--deep-burgundy);
            margin-bottom: 1rem;
        }

        .course-description {
            color: var(--black);
            opacity: 0.8;
            margin-bottom: 1.5rem;
        }

        .course-price {
            font-size: 1.2rem;
            color: var(--bronze);
            font-weight: bold;
        }

        /* Contact Section */
        .contact {
            padding: 6rem 0;
            background: var(--deep-burgundy);
            color: var(--white);
        }

        .contact-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            text-align: center;
        }

        .contact-title {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: var(--champagne);
        }

        .contact-info {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .address {
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 15px;
            margin: 2rem auto;
            max-width: 600px;
            backdrop-filter: blur(10px);
        }

        /* Footer */
        .footer {
            background: var(--black);
            color: var(--white);
            padding: 3rem 0;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .hero-text h1 {
                font-size: 2.5rem;
            }
            
            .founders-grid {
                grid-template-columns: 1fr;
            }
            
            .courses-grid {
                grid-template-columns: 1fr;
            }

            .nav-links {
                display: none;
            }
        }

        /* Animations */
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

        .fade-in {
            animation: fadeInUp 0.8s ease forwards;
        }

        /* Scroll animations */
        .scroll-reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }

        .scroll-reveal.revealed {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <nav class="nav-container">
            <div class="logo">
                <div class="logo-icon"></div>
                <div class="logo-text">WingLash</div>
            </div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#courses">Courses</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <div class="hero-text fade-in">
                <h1>Master the Art of <span class="highlight">Professional Makeup</span></h1>
                <p>Transform your passion into expertise with WingLash Academy's comprehensive makeup courses. Learn from globally certified professionals and elevate your artistry to new heights.</p>
                <a href="#courses" class="cta-button">Explore Courses</a>
            </div>
            <div class="hero-visual">
                <div class="makeup-showcase"></div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about scroll-reveal" id="about">
        <div class="about-container">
            <h2 class="section-title">Meet Our Expert Founders</h2>
            <div class="founders-grid">
                <div class="founder-card">
                    <div class="founder-avatar khushbu"></div>
                    <h3 class="founder-name">Ms. Khushbu Sharma</h3>
                    <p class="founder-title">Co-Founder & Lead Instructor</p>
                    <p class="founder-description">Highly experienced and globally certified makeup artist by CIDESCO International. Specializes in bridal makeup with years of expertise in creating stunning, timeless looks that enhance natural beauty and celebrate special moments.</p>
                    <div class="social-links">
                        <a href="https://instagram.com/muakhushbu" target="_blank" class="instagram-link">
                            <svg class="instagram-icon" viewBox="0 0 24 24">
                                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                            </svg>
                            @muakhushbu
                        </a>
                    </div>
                </div>
                <div class="founder-card">
                    <div class="founder-avatar shruti"></div>
                    <h3 class="founder-name">Ms. Shruti Agarwal</h3>
                    <p class="founder-title">Co-Founder & Professional Artist</p>
                    <p class="founder-description">Professional makeup artist with global certification, specializing in bridal, fashion, and artistic makeup. Brings creativity and technical excellence to every look, ensuring students learn both foundational skills and advanced techniques.</p>
                    <div class="social-links">
                        <a href="https://instagram.com/shrutiagarwalmakeup" target="_blank" class="instagram-link">
                            <svg class="instagram-icon" viewBox="0 0 24 24">
                                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                            </svg>
                            @shrutiagarwalmakeup
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Courses Section -->
    <section class="courses scroll-reveal" id="courses">
        <div class="courses-container">
            <h2 class="section-title">Professional Makeup Courses</h2>
            <div class="courses-grid">
                <div class="course-card">
                    <div class="course-image"></div>
                    <div class="course-content">
                        <h3 class="course-title">Bridal Makeup Mastery</h3>
                        <p class="course-description">Complete bridal makeup course covering traditional and contemporary styles, color theory, and advanced techniques for creating perfect wedding looks.</p>
                        <div class="course-price">Starting from ₹25,000</div>
                    </div>
                </div>
                <div class="course-card">
                    <div class="course-image"></div>
                    <div class="course-content">
                        <h3 class="course-title">Professional Makeup Artist</h3>
                        <p class="course-description">Comprehensive program covering all aspects of professional makeup artistry, from basic techniques to advanced editorial and fashion makeup.</p>
                        <div class="course-price">Starting from ₹35,000</div>
                    </div>
                </div>
                <div class="course-card">
                    <div class="course-image"></div>
                    <div class="course-content">
                        <h3 class="course-title">Makeup Foundation Course</h3>
                        <p class="course-description">Perfect for beginners, this course covers fundamental makeup techniques, skin preparation, color matching, and basic application skills.</p>
                        <div class="course-price">Starting from ₹15,000</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact scroll-reveal" id="contact">
        <div class="contact-container">
            <h2 class="contact-title">Start Your Makeup Journey</h2>
            <p class="contact-info">Ready to transform your passion into profession? Get in touch with us today!</p>
            <div class="address">
                <h3>Visit Our Academy</h3>
                <p>WingLash Pvt Ltd<br>
                Shashi Shekar Bose Row<br>
                Bhawanipur, Kolkata- 700025</p>
            </div>
            <a href="tel:+91XXXXXXXXXX" class="cta-button">Call Now</a>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="footer-content">
            <div class="logo">
                <div class="logo-icon"></div>
                <div class="logo-text">WingLash</div>
            </div>
            <p>&copy; 2025 WingLash Pvt Ltd. All rights reserved. | Professional Makeup Academy</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Scroll reveal animation
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('revealed');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.scroll-reveal').forEach(el => {
            observer.observe(el);
        });

        // Header background change on scroll
        window.addEventListener('scroll', function() {
            const header = document.querySelector('.header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(26, 26, 26, 0.98)';
            } else {
                header.style.background = 'rgba(26, 26, 26, 0.95)';
            }
        });

        // Add floating animation to course cards
        document.querySelectorAll('.course-card').forEach((card, index) => {
            card.style.animationDelay = `${index * 0.2}s`;
            card.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-15px) scale(1.02)';
            });
            card.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0) scale(1)';
            });
        });

        // Founder card hover effects
        document.querySelectorAll('.founder-card').forEach(card => {
            card.addEventListener('mouseenter', function() {
                this.querySelector('.founder-avatar').style.transform = 'scale(1.05)';
                this.querySelector('.founder-avatar').style.boxShadow = '0 15px 40px rgba(232, 180, 160, 0.5)';
            });
            card.addEventListener('mouseleave', function() {
                this.querySelector('.founder-avatar').style.transform = 'scale(1)';
                this.querySelector('.founder-avatar').style.boxShadow = '0 10px 30px rgba(232, 180, 160, 0.3)';
            });
        });
    </script>
</body>
</html>
