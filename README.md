<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beveridge-Neff Woodshop | Monongahela, PA</title>
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #8B4513;
            --secondary: #D2691E;
            --accent: #FFD700;
            --dark: #2C1810;
            --light: #F5F5DC;
            --wood-dark: #4A3728;
            --wood-light: #8B6F47;
            --forest: #228B22;
            --rust: #B7410E;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #f5f5dc 0%, #e8dcc4 50%, #d4c4a8 100%);
            color: var(--dark);
            overflow-x: hidden;
        }

        header {
            background: linear-gradient(90deg, var(--wood-dark) 0%, var(--primary) 50%, var(--wood-dark) 100%);
            padding: 1rem 0;
            box-shadow: 0 4px 20px rgba(0,0,0,0.3);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-content {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .logo-section {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .logo-img {
            width: 100px;
            height: 60px;
            background: white;
            border-radius: 4px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            color: var(--dark);
            border: 3px solid var(--accent);
            font-weight: bold;
        }

        .brand-text h1 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 2.2rem;
            color: white;
            letter-spacing: 2px;
        }

        .brand-text p {
            color: var(--accent);
            font-size: 0.9rem;
            font-weight: 600;
        }

        .hours-badge {
            background: var(--accent);
            color: var(--dark);
            padding: 0.5rem 1rem;
            border-radius: 25px;
            font-weight: 700;
            font-size: 0.9rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

        nav {
            background: rgba(44, 24, 16, 0.95);
            padding: 1rem 0;
            backdrop-filter: blur(10px);
        }

        .nav-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
        }

        .nav-btn {
            background: linear-gradient(145deg, var(--secondary), var(--rust));
            color: white;
            border: none;
            padding: 1rem 2rem;
            font-size: 1.1rem;
            font-weight: 700;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
            box-shadow: 0 4px 15px rgba(178, 65, 14, 0.4);
        }

        .nav-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(178, 65, 14, 0.6);
        }

        .nav-btn.active {
            background: linear-gradient(145deg, var(--forest), #1a6b1a);
        }

        main {
            max-width: 1400px;
            margin: 0 auto;
            padding: 2rem;
            min-height: 70vh;
        }

        .section {
            display: none;
            animation: fadeIn 0.5s ease-in;
        }

        .section.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hero {
            text-align: center;
            padding: 3rem 0;
            background: linear-gradient(135deg, rgba(139, 69, 19, 0.1) 0%, rgba(210, 105, 30, 0.1) 100%);
            border-radius: 20px;
            margin-bottom: 2rem;
            border: 3px solid var(--wood-light);
        }

        .hero h2 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 3.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.3rem;
            color: var(--wood-dark);
            max-width: 800px;
            margin: 0 auto 2rem;
            line-height: 1.8;
        }

        .contact-highlight {
            background: linear-gradient(145deg, var(--accent), #FFA500);
            color: var(--dark);
            padding: 1.5rem 3rem;
            border-radius: 15px;
            display: inline-block;
            font-size: 1.5rem;
            font-weight: 700;
            box-shadow: 0 6px 20px rgba(255, 215, 0, 0.4);
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .portfolio-item {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            transition: transform 0.3s ease;
            border: 3px solid var(--wood-light);
        }

        .portfolio-item:hover {
            transform: translateY(-10px);
        }

        .portfolio-img {
            width: 100%;
            height: 250px;
            background: linear-gradient(135deg, var(--wood-light) 0%, var(--primary) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
            font-weight: bold;
        }

        .portfolio-info {
            padding: 1.5rem;
        }

        .portfolio-info h3 {
            color: var(--primary);
            margin-bottom: 0.5rem;
            font-size: 1.3rem;
        }

        .booking-section {
            text-align: center;
            padding: 4rem 2rem;
            background: linear-gradient(135deg, var(--forest) 0%, #1a6b1a 100%);
            border-radius: 20px;
            color: white;
            margin-top: 2rem;
        }

        .booking-section h2 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .phone-number {
            font-size: 3rem;
            font-weight: 700;
            color: var(--accent);
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            margin: 1rem 0;
            display: inline-block;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .worker-login {
            max-width: 500px;
            margin: 0 auto;
            background: white;
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.2);
            border: 3px solid var(--primary);
        }

        .worker-login h2 {
            color: var(--primary);
            margin-bottom: 2rem;
            text-align: center;
            font-family: 'Bebas Neue', sans-serif;
            font-size: 2.5rem;
        }

        .password-input {
            width: 100%;
            padding: 1rem;
            font-size: 1.2rem;
            border: 3px solid var(--wood-light);
            border-radius: 10px;
            margin-bottom: 1rem;
            text-align: center;
            letter-spacing: 2px;
        }

        .submit-btn {
            width: 100%;
            padding: 1rem;
            background: linear-gradient(145deg, var(--primary), var(--secondary));
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 1.2rem;
            font-weight: 700;
            cursor: pointer;
            transition: transform 0.2s;
        }

        .submit-btn:hover {
            transform: scale(1.02);
        }

        .error-msg {
            color: #dc3545;
            text-align: center;
            margin-top: 1rem;
            font-weight: 600;
        }

        .appointments-panel {
            background: white;
            border-radius: 20px;
            padding: 2rem;
            box-shadow: 0 10px 40px rgba(0,0,0,0.2);
        }

        .appointments-panel h2 {
            color: var(--primary);
            margin-bottom: 2rem;
            font-family: 'Bebas Neue', sans-serif;
            font-size: 2.5rem;
            text-align: center;
        }

        .add-appointment-btn {
            background: linear-gradient(145deg, var(--forest), #1a6b1a);
            color: white;
            border: none;
            padding: 1rem 2rem;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 700;
            cursor: pointer;
            margin-bottom: 2rem;
            display: block;
            margin-left: auto;
            margin-right: auto;
        }

        .appointment-form {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 2rem;
            border-radius: 15px;
            margin-bottom: 2rem;
            border: 2px solid var(--wood-light);
            display: none;
        }

        .appointment-form.active {
            display: block;
            animation: slideDown 0.3s ease;
        }

        @keyframes slideDown {
            from { opacity: 0; max-height: 0; }
            to { opacity: 1; max-height: 1000px; }
        }

        .form-group {
            margin-bottom: 1rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--dark);
        }

        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 2px solid var(--wood-light);
            border-radius: 8px;
            font-size: 1rem;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        .appointments-list {
            display: grid;
            gap: 1rem;
        }

        .appointment-card {
            background: linear-gradient(135deg, #fff 0%, #f8f9fa 100%);
            border-left: 5px solid var(--primary);
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            display: grid;
            grid-template-columns: 1fr auto;
            gap: 1rem;
            align-items: center;
        }

        .appointment-info h3 {
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .appointment-details {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            font-size: 0.9rem;
            color: #666;
        }

        .appointment-details span {
            background: var(--light);
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
        }

        .total-badge {
            background: linear-gradient(145deg, var(--accent), #FFA500);
            color: var(--dark);
            padding: 0.8rem 1.5rem;
            border-radius: 10px;
            font-weight: 700;
            font-size: 1.2rem;
            text-align: center;
        }

        .payment-method {
            background: var(--forest);
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.8rem;
            margin-top: 0.5rem;
            display: inline-block;
        }

        .delete-btn {
            background: #dc3545;
            color: white;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            cursor: pointer;
            font-size: 0.9rem;
        }

        footer {
            background: var(--wood-dark);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
        }

        .footer-content {
            max-width: 1400px;
            margin: 0 auto;
        }

        .footer-phone {
            font-size: 1.5rem;
            color: var(--accent);
            font-weight: 700;
            margin: 1rem 0;
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }

            .hero h2 {
                font-size: 2rem;
            }

            .phone-number {
                font-size: 1.8rem;
            }

            .form-row {
                grid-template-columns: 1fr;
            }

            .appointment-card {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <div class="logo-section">
                <div class="logo-img">LOGO</div>
                <div class="brand-text">
                    <h1>BEVERIDGE-NEFF WOODSHOP</h1>
                    <p>MONONGAHELA, PA | EST. 2026</p>
                </div>
            </div>
            <div class="hours-badge">OPEN 9AM - 5PM</div>
        </div>
    </header>

    <nav>
        <div class="nav-container">
            <button class="nav-btn active" onclick="showSection('about')">About Us</button>
            <button class="nav-btn" onclick="showSection('book')">Book Appointment</button>
            <button class="nav-btn" onclick="showSection('workers')">Workers Portal</button>
        </div>
    </nav>

    <main>
        <!-- About Us Section -->
        <section id="about" class="section active">
            <div class="hero">
                <h2>Craftsmanship That Stands the Test of Time</h2>
                <p>Welcome to Beveridge-Neff Woodshop, where traditional craftsmanship meets modern precision. Founded in 2026 in the heart of Monongahela, Pennsylvania, we are dedicated to creating beautiful, handcrafted wooden pieces that become heirlooms for generations.</p>
                <p>Our skilled artisans bring decades of combined experience to every project, from custom furniture and cabinetry to intricate woodturning and restoration work. We source only the finest hardwoods, including locally harvested Pennsylvania cherry, walnut, and oak, ensuring each piece tells a story of quality and sustainability.</p>
                <p>Whether you are looking for a custom dining table, built-in shelving, or a unique gift, we work closely with you to bring your vision to life. Every cut, joint, and finish is executed with meticulous attention to detail.</p>
                <div class="contact-highlight">Call Today: (724) 825-5886</div>
            </div>

            <h2 style="text-align: center; color: var(--primary); font-family: 'Bebas Neue', sans-serif; font-size: 2.5rem; margin: 2rem 0;">Our Portfolio</h2>

            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <div class="portfolio-img">Custom Dining Table</div>
                    <div class="portfolio-info">
                        <h3>Handcrafted Dining Table</h3>
                        <p>Solid walnut with traditional mortise and tenon joinery. Custom stained finish.</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-img">Rustic Bookshelf</div>
                    <div class="portfolio-info">
                        <h3>Reclaimed Barn Wood Shelf</h3>
                        <p>Made from 100-year-old Pennsylvania barn wood with industrial iron brackets.</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-img">Kitchen Cabinets</div>
                    <div class="portfolio-info">
                        <h3>Custom Cherry Cabinetry</h3>
                        <p>Full kitchen remodel with hand-rubbed oil finish and soft-close hardware.</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-img">Rocking Chair</div>
                    <div class="portfolio-info">
                        <h3>Hand-Turned Rocking Chair</h3>
                        <p>Classic design in maple with woven cane seat. Perfect for the front porch.</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-img">Jewelry Box</div>
                    <div class="portfolio-info">
                        <h3>Intarsia Jewelry Box</h3>
                        <p>Small keepsake box with intricate wood inlay patterns and velvet lining.</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-img">Coffee Table</div>
                    <div class="portfolio-info">
                        <h3>Live Edge Coffee Table</h3>
                        <p>Natural edge slab with hairpin legs. Preserved bark texture with epoxy fill.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Book Appointment Section -->
        <section id="book" class="section">
            <div class="booking-section">
                <h2>Ready to Start Your Project?</h2>
                <p style="font-size: 1.3rem; margin-bottom: 2rem;">We would love to hear about your woodworking needs. Give us a call or send a text to schedule your consultation!</p>
                <div class="phone-number">(724) 825-5886</div>
                <p style="margin-top: 2rem; font-size: 1.1rem;">Hours: Monday - Friday, 9:00 AM - 5:00 PM</p>
                <p style="margin-top: 1rem;">Located in Monongahela, PA</p>
            </div>

            <div style="text-align: center; margin-top: 3rem; padding: 2rem; background: white; border-radius: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
                <h3 style="color: var(--primary); margin-bottom: 1rem; font-size: 1.8rem;">What to Expect</h3>
                <p style="font-size: 1.1rem; line-height: 1.8; max-width: 600px; margin: 0 auto;">
                    When you call, we will discuss your project ideas, timeline, and budget. We offer free estimates and can work from your sketches, photos, or just a description of what you have in mind. 
                </p>
            </div>
        </section>

        <!-- Workers Portal Section -->
        <section id="workers" class="section">
            <div id="loginPanel" class="worker-login">
                <h2>Workers Portal</h2>
                <p style="text-align: center; margin-bottom: 2rem; color: #666;">Authorized Personnel Only</p>
                <input type="password" id="passwordInput" class="password-input" placeholder="ENTER PASSCODE">
                <button class="submit-btn" onclick="checkPassword()">Access Portal</button>
                <p id="errorMsg" class="error-msg"></p>
            </div>

            <div id="appointmentsPanel" class="appointments-panel" style="display: none;">
                <h2>Appointment Management</h2>
                <button class="add-appointment-btn" onclick="toggleForm()">+ Add New Appointment</button>

                <div id="appointmentForm" class="appointment-form">
                    <h3 style=
