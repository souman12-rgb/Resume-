
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Souman Das | BBA DBE Student</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Playfair+Display:wght@400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --gray: #95a5a6;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: var(--primary);
            color: white;
            padding: 2rem 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(44,62,80,0.9) 0%, rgba(52,152,219,0.7) 100%);
            z-index: 1;
        }
        
        header .container {
            position: relative;
            z-index: 2;
        }
        
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }
        
        .title {
            font-weight: 300;
            font-size: 1.2rem;
            margin-bottom: 1rem;
        }
        
        .contact-info {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 1rem;
            flex-wrap: wrap;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .contact-item i {
            font-size: 1.1rem;
        }
        
        /* Navigation */
        nav {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .navbar {
            display: flex;
            justify-content: center;
            list-style: none;
            padding: 1rem 0;
        }
        
        .navbar li {
            margin: 0 1.5rem;
        }
        
        .navbar a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            font-size: 1rem;
            transition: color 0.3s;
            position: relative;
            padding: 0.5rem 0;
        }
        
        .navbar a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--secondary);
            transition: width 0.3s;
        }
        
        .navbar a:hover {
            color: var(--secondary);
        }
        
        .navbar a:hover::after {
            width: 100%;
        }
        
        /* Section Styles */
        section {
            padding: 4rem 0;
        }
        
        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            text-align: center;
            margin-bottom: 2rem;
            color: var(--primary);
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background-color: var(--secondary);
            margin: 0.5rem auto;
        }
        
        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 3rem;
        }
        
        .profile-img {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .profile-img img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .about-text {
            flex: 2;
        }
        
        /* Education Section */
        .education-item {
            background-color: white;
            padding: 1.5rem;
            border-radius: 8px;
            margin-bottom: 1.5rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
            border-left: 4px solid var(--secondary);
        }
        
        .education-item h3 {
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .education-item .date {
            color: var(--gray);
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }
        
        /* Experience Section */
        .experience-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .experience-card {
            background-color: white;
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .experience-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .experience-card h3 {
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .experience-card .company {
            color: var(--secondary);
            font-weight: 600;
            margin-bottom: 0.5rem;
        }
        
        .experience-card .date {
            color: var(--gray);
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }
        
        .experience-card ul {
            padding-left: 1.5rem;
        }
        
        .experience-card li {
            margin-bottom: 0.5rem;
        }
        
        /* Skills Section */
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
        }
        
        .skill-tag {
            background-color: var(--secondary);
            color: white;
            padding: 0.5rem 1.2rem;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
        }
        
        /* Contact Section */
        .contact-section {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
            margin-top: 2rem;
        }
        
        .contact-methods {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 2rem;
            margin-top: 1.5rem;
        }
        
        .contact-method {
            text-align: center;
            flex: 1;
            min-width: 200px;
        }
        
        .contact-method i {
            font-size: 2rem;
            color: var(--secondary);
            margin-bottom: 1rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--primary);
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 2rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--secondary);
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .about-content {
                flex-direction: column;
            }
            
            .navbar {
                flex-direction: column;
                align-items: center;
                gap: 1rem;
            }
            
            .navbar li {
                margin: 0.5rem 0;
            }
            
            .contact-info {
                flex-direction: column;
                gap: 0.5rem;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Souman Das</h1>
            <p class="title">BBA in Digital Business & Entrepreneurship | 2024-27</p>
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>soumand24@iimb.ac.in</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <span>+91 1234567890</span>
                </div>
            </div>
        </div>
    </header>
    
    <nav>
        <ul class="navbar">
            <li><a href="#about">About</a></li>
            <li><a href="#education">Education</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    
    <main class="container">
        <section id="about">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="profile-img">
                    <!-- Placeholder for profile image - replace with actual image -->
                    <img src="https://via.placeholder.com/400x500" alt="Souman Das">
                </div>
                <div class="about-text">
                    <p>Hello! I'm Souman Das, a passionate and driven student pursuing a Bachelor's in Business Administration with a specialization in Digital Business & E-Commerce (2024-2027). I'm fascinated by the intersection of business and technology and how digital transformation is reshaping industries.</p>
                    <p>With a strong academic foundation and practical experience in digital marketing and e-commerce operations, I'm developing skills to thrive in the digital economy. I'm particularly interested in data-driven decision making, customer experience optimization, and digital business models.</p>
                    <p>Feel free to reach out to me at <strong>soumand24@iimb.ac.in</strong> or call me at <strong>+91 1234567890</strong> for any opportunities or collaborations.</p>
                </div>
            </div>
        </section>
        
        <section id="education">
            <h2 class="section-title">Education</h2>
            <div class="education-item">
                <h3>Bachelor of Business Administration (BBA) - Digital Business & E-Commerce</h3>
                <p class="date">2024 - 2027 (Expected)</p>
                <p>Currently pursuing a specialized degree focusing on digital business models, e-commerce strategies, digital marketing, and data analytics for business decision making.</p>
            </div>
            <div class="education-item">
                <h3>Higher Secondary Education (Commerce Stream)</h3>
                <p class="date">2022 - 2024</p>
                <p>Completed with distinction, focusing on business studies, economics, accountancy, and mathematics.</p>
            </div>
        </section>
        
        <section id="experience">
            <h2 class="section-title">Experience</h2>
            <div class="experience-grid">
                <div class="experience-card">
                    <h3>Digital Marketing Intern</h3>
                    <p class="company">E-Commerce Startup (Remote)</p>
                    <p class="date">Summer 2024</p>
                    <ul>
                        <li>Assisted in developing and implementing social media marketing strategies</li>
                        <li>Created content for various digital platforms increasing engagement by 35%</li>
                        <li>Analyzed campaign performance using Google Analytics</li>
                        <li>Conducted competitor research and market analysis</li>
                    </ul>
                </div>
                <div class="experience-card">
                    <h3>E-Commerce Assistant</h3>
                    <p class="company">Local Retail Business</p>
                    <p class="date">Part-time, 2023-2024</p>
                    <ul>
                        <li>Managed product listings on e-commerce platforms (Amazon, Flipkart)</li>
                        <li>Optimized product descriptions and images leading to 20% increase in conversions</li>
                        <li>Handled customer inquiries and order processing</li>
                        <li>Assisted in inventory management and logistics coordination</li>
                    </ul>
                </div>
                <div class="experience-card">
                    <h3>Freelance Content Creator</h3>
                    <p class="company">Self-Employed</p>
                    <p class="date">2022-Present</p>
                    <ul>
                        <li>Create blog content on digital business trends and e-commerce strategies</li>
                        <li>Develop social media content for small businesses</li>
                        <li>Manage basic SEO optimization for client websites</li>
                        <li>Design simple graphics and marketing materials using Canva</li>
                    </ul>
                </div>
            </div>
        </section>
        
        <section id="skills">
            <h2 class="section-title">Skills</h2>
            <div class="skills-container">
                <span class="skill-tag">Digital Marketing</span>
                <span class="skill-tag">E-Commerce</span>
                <span class="skill-tag">Social Media Management</span>
                <span class="skill-tag">Content Creation</span>
                <span class="skill-tag">Google Analytics</span>
                <span class="skill-tag">SEO Basics</span>
                <span class="skill-tag">Market Research</span>
                <span class="skill-tag">Data Analysis</span>
                <span class="skill-tag">Microsoft Office</span>
                <span class="skill-tag">Canva</span>
                <span class="skill-tag">HTML/CSS Basics</span>
                <span class="skill-tag">Communication</span>
                <span class="skill-tag">Project Management</span>
            </div>
        </section>
        
        <section id="contact">
            <h2 class="section-title">Contact Me</h2>
            <div class="contact-section">
                <p>I'm always open to discussing new opportunities, collaborations, or just chatting about digital business trends. Here's how you can reach me:</p>
                
                <div class="contact-methods">
                    <div class="contact-method">
                        <i class="fas fa-envelope"></i>
                        <h3>Email</h3>
                        <p>soumand24@iimb.ac.in</p>
                    </div>
                    
                    <div class="contact-method">
                        <i class="fas fa-phone"></i>
                        <h3>Phone</h3>
                        <p>+91 1234567890</p>
                    </div>
                    
                    <div class="contact-method">
                        <i class="fas fa-map-marker-alt"></i>
                        <h3>Location</h3>
                        <p>Bangalore, India</p>
                    </div>
                </div>
            </div>
        </section>
    </main>
    
    <footer>
        <div class="container">
            <h3>Get In Touch</h3>
            <div class="social-links">
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="mailto:soumand24@iimb.ac.in"><i class="fas fa-envelope"></i></a>
            </div>
            <p>&copy; 2024 Souman Das. All rights reserved.</p>
            <p class="footer-contact">Email: soumand24@iimb.ac.in | Phone: +91 1234567890</p>
        </div>
    </footer>
    
    <!-- Font Awesome for icons (add this before closing body tag) -->
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</body>
</html>
