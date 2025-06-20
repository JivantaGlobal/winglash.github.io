```html
 <!DOCTYPE html>
 <html lang="en">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jivanta Global - Premium Agricultural Trading</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap');
 

  * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  }

  body {
  font-family: 'Poppins', sans-serif;
  color: #333;
  overflow-x: hidden;
  background: #f8f8f8;
  }

  .container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 30px;
  }

  /* Header & Navigation */
  header {
  background: rgba(20, 83, 45, 0.9);
  color: white;
  padding: 1rem 0;
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 1000;
  backdrop-filter: blur(10px);
  transition: all 0.4s ease;
  box-shadow: 0 5px 30px rgba(0,0,0,0.1);
  }

  header.scrolled {
  padding: 0.5rem 0;
  background: rgba(20, 83, 45, 0.95);
  }

  nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  }

  .logo {
  display: flex;
  align-items: center;
  gap: 15px;
  }

  .logo-icon {
  width: 50px;
  height: 50px;
  background: linear-gradient(45deg, #4CAF50, #8BC34A);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  font-weight: bold;
  color: white;
  box-shadow: 0 4px 15px rgba(76, 175, 80, 0.3);
  }

  .logo h1 {
  font-size: 1.8rem;
  font-weight: 700;
  background: linear-gradient(45deg, #ffffff, #e8f5e8);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  }

  .nav-links {
  display: flex;
  list-style: none;
  gap: 2rem;
  }

  .nav-links a {
  color: white;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s ease;
  padding: 8px 16px;
  border-radius: 6px;
  position: relative;
  }

  .nav-links a::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: white;
  transition: width 0.3s ease;
  }

  .nav-links a:hover::after {
  width: 100%;
  }

  .mobile-menu-btn {
  display: none;
  background: none;
  border: none;
  color: white;
  font-size: 1.5rem;
  cursor: pointer;
  }

  /* Hero Section */
  .hero {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
  url('http://googleusercontent.com/image_generation_content/1');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  min-height: 100vh;
  display: flex;
  align-items: center;
  text-align: center;
  color: white;
  position: relative;
  }

  .hero-content h2 {
  font-size: 4rem;
  margin-bottom: 1.5rem;
  font-weight: 800;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
  animation: fadeInUp 1s ease-out;
  line-height: 1.2;
  }

  .hero-content p {
  font-size: 1.5rem;
  margin-bottom: 2.5rem;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
  opacity: 0.95;
  animation: fadeInUp 1s ease-out 0.3s both;
  }

  .cta-button {
  display: inline-block;
  background: linear-gradient(45deg, #4CAF50, #66BB6A);
  color: white;
  padding: 18px 40px;
  text-decoration: none;
  border-radius: 50px;
  font-weight: 600;
  font-size: 1.2rem;
  transition: all 0.3s ease;
  box-shadow: 0 8px 25px rgba(76, 175, 80, 0.4);
  animation: fadeInUp 1s ease-out 0.6s both;
  position: relative;
  overflow: hidden;
  }

  .cta-button::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
  transition: 0.5s;
  }

  .cta-button:hover::before {
  left: 100%;
  }

  .cta-button:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 35px rgba(76, 175, 80, 0.6);
  }

  /* Floating Particles */
  .particles {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  z-index: 1;
  }

  .particle {
  position: absolute;
  display: block;
  background: rgba(255,255,255,0.2);
  border-radius: 50%;
  animation: animate 15s linear infinite;
  bottom: -150px;
  }

  .particle:nth-child(1) {
  left: 25%;
  width: 80px;
  height: 80px;
  animation-delay: 0s;
  }

  .particle:nth-child(2) {
  left: 10%;
  width: 20px;
  height: 20px;
  animation-delay: 2s;
  animation-duration: 12s;
  }

  .particle:nth-child(3) {
  left: 70%;
  width: 20px;
  height: 20px;
  animation-delay: 4s;
  }

  .particle:nth-child(4) {
  left: 40%;
  width: 60px;
  height: 60px;
  animation-delay: 0s;
  animation-duration: 18s;
  }

  .particle:nth-child(5) {
  left: 65%;
  width: 20px;
  height: 20px;
  animation-delay: 0s;
  }

  .particle:nth-child(6) {
  left: 75%;
  width: 110px;
  height: 110px;
  animation-delay: 3s;
  }

  .particle:nth-child(7) {
  left: 35%;
  width: 150px;
  height: 150px;
  animation-delay: 7s;
  }

  .particle:nth-child(8) {
  left: 50%;
  width: 25px;
  height: 25px;
  animation-delay: 15s;
  animation-duration: 45s;
  }

  .particle:nth-child(9) {
  left: 20%;
  width: 15px;
  height: 15px;
  animation-delay: 2s;
  animation-duration: 35s;
  }

  .particle:nth-child(10) {
  left: 85%;
  width: 150px;
  height: 150px;
  animation-delay: 0s;
  animation-duration: 11s;
  }

  @keyframes animate {
  0% {
  transform: translateY(0) rotate(0deg);
  opacity: 1;
  border-radius: 0;
  }
  100% {
  transform: translateY(-1000px) rotate(720deg);
  opacity: 0;
  border-radius: 50%;
  }
  }

  /* Products Section */
  .products {
  padding: 120px 0;
  background: #f8fffe;
  position: relative;
  }

  .section-title {
  text-align: center;
  font-size: 3.2rem;
  margin-bottom: 4rem;
  color: #2c5530;
  font-weight: 700;
  position: relative;
  display: inline-block;
  left: 50%;
  transform: translateX(-50%);
  }

  .section-title::after {
  content: '';
  position: absolute;
  width: 70%;
  height: 4px;
  background: linear-gradient(90deg, #4CAF50, #66BB6A, #81C784);
  bottom: -10px;
  left: 15%;
  border-radius: 2px;
  }

  .products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2.5rem;
  margin-top: 3rem;
  }

  .product-card {
  background: white;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 15px 50px rgba(0,0,0,0.1);
  transition: all 0.4s ease;
  position: relative;
  z-index: 1;
  }

  .product-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg, #4CAF50, #66BB6A, #81C784);
  }

  .product-card:hover {
  transform: translateY(-15px);
  box-shadow: 0 25px 70px rgba(0,0,0,0.15);
  }

  .product-image {
  height: 250px;
  overflow: hidden;
  }

  .product-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
  }

  .product-card:hover .product-image img {
  transform: scale(1.1);
  }

  .product-content {
  padding: 2rem;
  }

  .product-icon {
  width: 60px;
  height: 60px;
  background: linear-gradient(45deg, #4CAF50, #66BB6A);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 8px 25px rgba(76, 175, 80, 0.3);
  color: white;
  }

  .product-card h3 {
  font-size: 1.6rem;
  margin-bottom: 1rem;
  color: #2c5530;
  font-weight: 600;
  }

  .product-card p {
  color: #666;
  line-height: 1.6;
  margin-bottom: 1.5rem;
  }

  .product-specs {
  background: #f8f9fa;
  padding: 15px;
  border-radius: 10px;
  margin-top: 15px;
  border-left: 4px solid #4CAF50;
  }

  .product-specs li {
  margin-bottom: 8px;
  position: relative;
  padding-left: 20px;
  }

  .product-specs li::before {
  content: '✓';
  position: absolute;
  left: 0;
  color: #4CAF50;
  font-weight: bold;
  }

  /* About Section */
  .about {
  padding: 120px 0;
  background: linear-gradient(135deg, #2c5530 0%, #3e7b44 100%);
  color: white;
  position: relative;
  overflow: hidden;
  }

  .about::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path fill="rgba(255,255,255,0.02)" d="M0,0 L100,0 L100,100 L0,100 Z"></path></svg>');
  background-size: cover;
  opacity: 0.1;
  }

  .about-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
  position: relative;
  z-index: 1;
  }

  .about-text h2 {
  font-size: 2.8rem;
  margin-bottom: 2rem;
  font-weight: 700;
  position: relative;
  }

  .about-text h2::after {
  content: '';
  position: absolute;
  width: 100px;
  height: 4px;
  background: linear-gradient(90deg, #4CAF50, #66BB6A);
  bottom: -10px;
  left: 0;
  border-radius: 2px;
  }

  .about-text p {
  font-size: 1.2rem;
  line-height: 1.8;
  margin-bottom: 1.5rem;
  opacity: 0.95;
  }

  .stats {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
  margin-top: 3rem;
  }

  .stat-item {
  text-align: center;
  padding: 1.5rem;
  background: rgba(255,255,255,0.1);
  border-radius: 15px;
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
  border: 1px solid rgba(255,255,255,0.1);
  }

  .stat-item:hover {
  transform: translateY(-5px);
  background: rgba(255,255,255,0.15);
  }

  .stat-number {
  font-size: 2.8rem;
  font-weight: 800;
  color: #4CAF50;
  display: block;
  margin-bottom: 0.5rem;
  }

  .about-image {
  position: relative;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 20px 50px rgba(0,0,0,0.3);
  }

  .about-image img {
  width: 100%;
  height: auto;
  display: block;
  transition: transform 0.5s ease;
  }

  .about-image:hover img {
  transform: scale(1.05);
  }

  /* Contact Section */
  .contact {
  padding: 120px 0;
  background: #f8fffe;
  position: relative;
  }

  .contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  }

  .contact-info h3 {
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #2c5530;
  font-weight: 600;
  position: relative;
  }

  .contact-info h3::after {
  content: '';
  position: absolute;
  width: 80px;
  height: 4px;
  background: linear-gradient(90deg, #4CAF50, #66BB6A);
  bottom: -10px;
  left: 0;
  border-radius: 2px;
  }

  .contact-item {
  display: flex;
  align-items: center;
  gap: 1.5rem;
  margin-bottom: 1.5rem;
  padding: 1.5rem;
  background: white;
  border-radius: 15px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
  }

  .contact-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 40px rgba(0,0,0,0.1);
  }

  .contact-icon {
  width: 60px;
  height: 60px;
  background: linear-gradient(45deg, #4CAF50, #66BB6A);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 1.5rem;
  flex-shrink: 0;
  }

  .contact-details {
  flex-grow: 1;
  }

  .contact-details strong {
  display: block;
  margin-bottom: 0.5rem;
  color: #2c5530;
  }

  .contact-form {
  background: white;
  padding: 3rem;
  border-radius: 20px;
  box-shadow: 0 20px 50px rgba(0,0,0,0.1);
  position: relative;
  overflow: hidden;
  }

  .contact-form::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 5px;
  background: linear-gradient(90deg, #4CAF50, #66BB6A);
  }

  .contact-form h3 {
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #2c5530;
  font-weight: 600;
  position: relative;
  }

  .contact-form h3::after {
  content: '';
  position: absolute;
  width: 80px;
  height: 4px;
  background: linear-gradient(90deg, #4CAF50, #66BB6A);
  bottom: -10px;
  left: 0;
  border-radius: 2px;
  }

  .form-group {
  margin-bottom: 2rem;
  }

  .form-group label {
  display: block;
  font-size: 1.1rem;
  color: #555;
  margin-bottom: 0.5rem;
  }

  .form-group input,
  .form-group textarea {
  width: 100%;
  padding: 14px 20px;
  border: 1px solid #ddd;
  border-radius: 8px;
  font-size: 1rem;
  color: #333;
  transition: border-color 0.3s ease;
  }

  .form-group input:focus,
  .form-group textarea:focus {
  outline: none;
  border-color: #66BB6A;
  }

  .form-group textarea {
  height: 150px;
  resize: vertical;
  }

  .submit-btn {
  background: linear-gradient(45deg, #4CAF50, #66BB6A);
  color: white;
  padding: 16px 32px;
  border: none;
  border-radius: 50px;
  font-size: 1.1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 8px 25px rgba(76, 175, 80, 0.4);
  position: relative;
  overflow: hidden;
  display: inline-block;
  }

  .submit-btn::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
  transition: 0.5s;
  }

  .submit-btn:hover::before {
  left: 100%;
  }

  .submit-btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 30px rgba(76, 175, 80, 0.5);
  }

  /* Footer */
  footer {
  background: #2c5530;
  color: white;
  text-align: center;
  padding: 2rem 0;
  font-size: 0.9rem;
  position: relative;
  }

  footer::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 5px;
  background: linear-gradient(90deg, #4CAF50, #66BB6A, #81C784);
  }

  /* Responsive Styles */
  @media (max-width: 1024px) {
  .hero-content h2 {
  font-size: 3rem;
  }

  .hero-content p {
  font-size: 1.2rem;
  }

  .products-grid {
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  }

  .about-content {
  grid-template-columns: 1fr;
  text-align: center;
  }

  .about-image {
  order: -1;
  }

  .stats {
  grid-template-columns: 1fr;
  }

  .contact-content {
  grid-template-columns: 1fr;
  }
  }

  @media (max-width: 768px) {
  .nav-links {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  background: rgba(20, 83, 45, 0.95);
  flex-direction: column;
  text-align: center;
  padding: 1rem 0;
  box-shadow: 0 5px 15px rgba(0,0,0,0.2);
  }

  .nav-links.active {
  display: flex;
  }

  .nav-links a {
  padding: 12px 20px;
  display: block;
  }

  .mobile-menu-btn {
  display: block;
  }

  .hero-content h2 {
  font-size: 2.5rem;
  }

  .hero-content p {
  font-size: 1.1rem;
  }

  .section-title {
  font-size: 2.8rem;
  }

  .about-text h2 {
  font-size: 2.4rem;
  }

  .contact-form {
  padding: 2rem;
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
  </style>
 </head>
 <body>
  <header>
  <div class="container">
  <nav>
  <div class="logo">
  <div class="logo-icon">JG</div>
  <h1>Jivanta Global</h1>
  </div>
  <ul class="nav-links">
  <li><a href="#">Home</a></li>
  <li><a href="#">Products</a></li>
  <li><a href="#">About</a></li>
  <li><a href="#">Contact</a></li>
  </ul>
  <button class="mobile-menu-btn"><i class="fas fa-bars"></i></button>
  </nav>
  </div>
  </header>

  <section class="hero">
  <div class="particles">
  <div class="particle"></div>
  <div class="particle"></div>
  <div class="particle"></div>
  <div class="particle"></div>
  <div class="particle"></div>
  <div class="particle"></div>
  <div class="particle"></div>
  <div class="particle"></div>
  <div class="particle"></div>
  <div class="particle"></div>
  </div>
  <div class="container hero-content">
  <h2>Premium Agricultural Trading</h2>
  <p>Your trusted partner for high-quality agricultural products. We connect global markets with the finest
  harvests.</p>
  <a href="#" class="cta-button">Explore Our Products</a>
  </div>
  </section>

  <section class="products">
  <div class="container">
  <h2 class="section-title">Our Premium Products</h2>
  <div class="products-grid">
  <div class="product-card">
  <div class="product-image">
  <img src="http://googleusercontent.com/image_generation_content/0" alt="Premium Agricultural Product">
  </div>
  <div class="product-content">
  <div class="product-icon"><i class="fas fa-leaf"></i></div>
  <h3>Fresh Strawberries</h3>
  <p>Juicy and delicious strawberries, perfect for any occasion.</p>
  <ul class="product-specs">
  <li>High in antioxidants</li>
  <li>Rich in vitamins</li>
  <li>Sustainably grown</li>
  </ul>
  </div>
  </div>
  <div class="product-card">
  <div class="product-image">
  <img src="http://googleusercontent.com/image_generation_content/0" alt="Premium Agricultural Product">
  </div>
  <div class="product-content">
  <div class="product-icon"><i class="fas fa-wheat-alt"></i></div>
  <h3>Golden Wheat</h3>
  <p>Finest quality wheat, ideal for baking and more.</p>
  <ul class="product-specs">
  <li>High protein content</li>
  <li>Excellent for baking</li>
  <li>Organically farmed</li>
  </ul>
  </div>
  </div>
  <div class="product-card">
  <div class="product-image">
  <img src="http://googleusercontent.com/image_generation_content/0" alt="Premium Agricultural Product">
  </div>
  <div class="product-content">
  <div class="product-icon"><i class="fas fa-apple-alt"></i></div>
  <h3>Crisp Apples</h3>
  <p>Fresh and crisp apples, a healthy choice for everyone.</p>
  <ul class="product-specs">
  <li>Good source of fiber</li>
  <li>Naturally sweet</li>
  <li>Hand-picked quality</li>
  </ul>
  </div>
  </div>
  </div>
  </div>
  </section>

  <section class="about">
  <div class="container about-content">
  <div class="about-text">
  <h2>About Jivanta Global</h2>
  <p>Jivanta Global is committed to providing premium agricultural products to the global market. We
  partner with the best farms to ensure quality and sustainability.</p>
  <p>Our mission is to connect consumers with the freshest and finest harvests, promoting healthy
  living and supporting sustainable agriculture practices.</p>
  <div class="stats">
  <div class="stat-item">
  <span class="stat-number">100+</span>
  <span>Farms Partnered</span>
  </div>
  <div class="stat-item">
  <span class="stat-number">50+</span>
  <span>Products Available</span>
  </div>
  </div>
  </div>
  <div class="about-image">
  <img src="http://googleusercontent.com/image_generation_content/1" alt="Agricultural Land">
  </div>
  </div>
  </section>

  <section class="contact">
  <div class="container contact-content">
  <div class="contact-info">
  <h3>Contact Us</h3>
  <div class="contact-item">
  <div class="contact-icon"><i class="fas fa-map-marker-alt"></i></div>
  <div class="contact-details">
  <strong>Address:</strong>
  123 Agri Lane, Siliguri, WB, India
  </div>
  </div>
  <div class="contact-item">
  <div class="contact-icon"><i class="fas fa-phone"></i></div>
  <div class="contact-details">
  <strong>Phone:</strong>
  +91-9876543210
  </div>
  </div>
  <div class="contact-item">
  <div class="contact-icon"><i class="fas fa-envelope"></i></div>
  <div class="contact-details">
  <strong>Email:</strong>
  info@jivantaglobal.com
  </div>
  </div>
  </div>
  <div class="contact-form">
  <h3>Send us a Message</h3>
  <form>
  <div class="form-group">
  <label for="name">Your Name</label>
  <input type="text" id="name" name="name" placeholder="Your Name">
  </div>
  <div class="form-group">
  <label for="email">Your Email</label>
  <input type="email" id="email" name="email" placeholder="Your Email">
  </div>
  <div class="form-group">
  <label for="message">Message</label>
  <textarea id="message" name="message" placeholder="Your Message"></textarea>
  </div>
  <button type="submit
