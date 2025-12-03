# Travel_Agency

[index.html](https://github.com/user-attachments/files/23896610/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LuxeVoyage Travel Agency | Discover Your Next Journey</title>
    <!-- Elegant Google Fonts --><link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Lato:wght@300;400;700&display=swap" rel="stylesheet">
    
    <!-- Classy, Professional Internal CSS --><style>
        /* Color Palette & Typography */
        :root {
            --primary-gold: #c28b43; /* Rich Gold */
            --secondary-charcoal: #343a40; /* Dark Grey/Charcoal */
            --text-dark: #495057;
            --text-light: #6c757d;
            --bg-light: #f8f9fa; /* Off-white background */
            --bg-dark: #212529; /* Dark footer/accents */
            --border-light: #e9ecef;

            /* Fonts */
            --heading-font: 'Playfair Display', serif;
            --body-font: 'Lato', sans-serif;
        }

        body {
            font-family: var(--body-font);
            margin: 0;
            padding: 0;
            background-color: var(--bg-light); 
            color: var(--text-dark);
            line-height: 1.7;
            scroll-behavior: smooth;
        }
        
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header & Navigation */
        header {
            background-color: var(--bg-dark);
            color: white;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }
        header .logo {
            font-family: var(--heading-font);
            font-size: 28px;
            font-weight: 700;
            color: var(--primary-gold);
            cursor: pointer;
            text-decoration: none;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin-left: 25px;
            font-weight: 400;
            font-size: 16px;
            transition: color 0.3s ease;
        }
        nav a:hover {
            color: var(--primary-gold);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.6)), url('https://images.unsplash.com/photo-1501785888041-af3ba6f060d2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
            height: 60vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
            z-index: 1;
        }
        .hero-content h2 {
            font-family: var(--heading-font);
            font-size: 48px;
            margin-bottom: 15px;
            line-height: 1.2;
        }
        .hero-content p {
            font-size: 20px;
            margin-bottom: 30px;
            max-width: 700px;
            opacity: 0.9;
        }

        /* Section Styling */
        section {
            padding: 80px 0;
            border-bottom: 1px solid var(--border-light);
        }
        section:last-of-type {
            border-bottom: none;
        }
        section h2.section-title {
            font-family: var(--heading-font);
            font-size: 38px;
            text-align: center;
            color: var(--secondary-charcoal);
            margin-bottom: 20px;
            position: relative;
        }
        section h2.section-title::after {
            content: '';
            display: block;
            width: 70px;
            height: 3px;
            background-color: var(--primary-gold);
            margin: 15px auto 0;
            border-radius: 2px;
        }
        
        /* Buttons */
        .button {
            display: inline-block;
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            font-size: 16px;
            text-decoration: none;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .button.primary {
            background-color: var(--primary-gold);
            color: white;
        }
        .button.primary:hover {
            background-color: #a37237;
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }
        .button.secondary {
            background-color: var(--secondary-charcoal);
            color: white;
        }
        .button.secondary:hover {
            background-color: #495057;
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }

        /* Tour Packages */
        .package-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        .package-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .package-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }
        .package-card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
        }
        .package-content {
            padding: 25px;
        }
        .package-content h3 {
            font-family: var(--heading-font);
            font-size: 24px;
            color: var(--secondary-charcoal);
            margin-top: 0;
            margin-bottom: 10px;
        }
        .package-content p {
            font-size: 15px;
            color: var(--text-light);
            margin-bottom: 15px;
        }
        .package-price {
            font-size: 22px;
            font-weight: 700;
            color: var(--primary-gold);
            margin-bottom: 20px;
        }

        /* Destination Gallery */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-top: 50px;
        }
        .gallery-item {
            position: relative;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        .gallery-item:hover {
            transform: scale(1.03);
        }
        .gallery-item img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            display: block;
        }
        .gallery-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(transparent, rgba(0, 0, 0, 0.7));
            color: white;
            padding: 20px;
            font-family: var(--heading-font);
            font-size: 20px;
            font-weight: 700;
        }

        /* Travel Tips */
        .tips-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        .tip-card {
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.05);
            transition: box-shadow 0.3s ease;
        }
        .tip-card:hover {
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.1);
        }
        .tip-card h3 {
            font-family: var(--heading-font);
            font-size: 22px;
            color: var(--primary-gold);
            margin-top: 0;
            margin-bottom: 10px;
        }
        .tip-card p {
            font-size: 15px;
            color: var(--text-light);
        }

        /* Contact/Booking Form */
        .contact-form {
            max-width: 600px;
            margin: 50px auto 0;
            background-color: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        .contact-form label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--secondary-charcoal);
        }
        .contact-form input[type="text"],
        .contact-form input[type="email"],
        .contact-form input[type="tel"],
        .contact-form select,
        .contact-form textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 20px;
            border: 1px solid var(--border-light);
            border-radius: 5px;
            font-family: var(--body-font);
            font-size: 15px;
            box-sizing: border-box; /* Include padding in width */
            transition: border-color 0.3s ease;
        }
        .contact-form input:focus,
        .contact-form select:focus,
        .contact-form textarea:focus {
            border-color: var(--primary-gold);
            outline: none;
        }
        .contact-form textarea {
            resize: vertical;
            min-height: 100px;
        }
        .contact-form .button {
            width: 100%;
        }

        /* Footer */
        footer {
            background-color: var(--bg-dark);
            color: #ced4da;
            padding: 40px 0;
            text-align: center;
            font-size: 14px;
        }
        footer .social-links a {
            color: white;
            margin: 0 10px;
            font-size: 20px;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        footer .social-links a:hover {
            color: var(--primary-gold);
        }
        footer p {
            margin-top: 20px;
            margin-bottom: 0;
        }


        /* Responsive Adjustments */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            nav {
                margin-top: 15px;
            }
            nav a {
                margin: 0 10px;
                display: block;
                padding: 5px 0;
            }
            .hero-content h2 {
                font-size: 36px;
            }
            .hero-content p {
                font-size: 16px;
            }
            section h2.section-title {
                font-size: 32px;
            }
            .package-grid, .gallery-grid, .tips-grid {
                grid-template-columns: 1fr;
            }
            .container {
                padding: 15px;
            }
            .contact-form {
                padding: 25px;
            }
        }
        @media (max-width: 480px) {
            header .logo {
                font-size: 24px;
            }
            .hero-content h2 {
                font-size: 28px;
            }
            .hero-content p {
                font-size: 14px;
            }
            .button {
                padding: 10px 20px;
                font-size: 14px;
            }
            section h2.section-title {
                font-size: 28px;
            }
        }

    </style>
</head>
<body>

    <header>
        <div class="header-content">
            <a href="#home" class="logo">LuxeVoyage</a>
            <nav>
                <a href="#packages">Packages</a>
                <a href="#gallery">Destinations</a>
                <a href="#tips">Tips</a>
                <a href="#contact">Contact</a>
            </nav>
        </div>
    </header>

    <main id="app">
        <!-- Hero Section --><section id="home" class="hero">
            <div class="hero-content container">
                <h2>Your Journey to Unforgettable Memories Starts Here</h2>
                <p>Explore breathtaking destinations and craft your perfect adventure with LuxeVoyage, your trusted partner in luxury travel.</p>
                <a href="#packages" class="button primary">Discover Packages</a>
            </div>
        </section>

        <!-- Tour Packages Section --><section id="packages">
            <div class="container">
                <h2 class="section-title">Our Exclusive Tour Packages</h2>
                <p style="text-align: center; color: var(--text-light); margin-bottom: 40px;">Handpicked adventures for the discerning traveler.</p>
                
                <div class="package-grid">
                    <div class="package-card">
                        <img src="https://images.unsplash.com/photo-1528185567307-e817e90f2392?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Swiss Alps">
                        <div class="package-content">
                            <h3>Swiss Alps Adventure</h3>
                            <p>Experience the majestic beauty of the Swiss Alps with guided hikes, pristine lakes, and charming villages.</p>
                            <div class="package-price">₹1,80,000 / person</div>
                            <a href="#contact" class="button primary">Book Now</a>
                        </div>
                    </div>

                    <div class="package-card">
                        <img src="https://images.unsplash.com/photo-1549479369-0294d1830491?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Thai Beaches">
                        <div class="package-content">
                            <h3>Exotic Thailand Retreat</h3>
                            <p>Relax on the pristine beaches of Thailand, explore ancient temples, and indulge in exquisite cuisine.</p>
                            <div class="package-price">₹1,20,000 / person</div>
                            <a href="#contact" class="button primary">Book Now</a>
                        </div>
                    </div>

                    <div class="package-card">
                        <img src="https://images.unsplash.com/photo-1524850175822-e2c72b21cfb0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Rajasthan Heritage">
                        <div class="package-content">
                            <h3>Royal Rajasthan Heritage Tour</h3>
                            <p>Discover the vibrant history and royal grandeur of Rajasthan's palaces, forts, and deserts.</p>
                            <div class="package-price">₹95,000 / person</div>
                            <a href="#contact" class="button primary">Book Now</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Destination Gallery Section --><section id="gallery" style="background-color: var(--bg-light);">
            <div class="container">
                <h2 class="section-title">Inspiring Travel Destinations</h2>
                <p style="text-align: center; color: var(--text-light); margin-bottom: 40px;">A glimpse into the wonders awaiting your exploration.</p>
                
                <div class="gallery-grid">
                    <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1523978593390-336294713c71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Paris">
                        <div class="gallery-overlay">Paris, France</div>
                    </div>
                    <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1557007469-ab08832a8a81?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Maldives">
                        <div class="gallery-overlay">Maldives</div>
                    </div>
                    <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1589139031753-27038d1ee7ae?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Kyoto">
                        <div class="gallery-overlay">Kyoto, Japan</div>
                    </div>
                     <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1507525428034-b723cf961fac?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Bora Bora">
                        <div class="gallery-overlay">Bora Bora</div>
                    </div>
                    <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1580671607519-7023190a6184?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Rome">
                        <div class="gallery-overlay">Rome, Italy</div>
                    </div>
                    <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1522079085816-72f3e803c002?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Cappadocia">
                        <div class="gallery-overlay">Cappadocia, Turkey</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Travel Tips Section --><section id="tips">
            <div class="container">
                <h2 class="section-title">Essential Travel Tips</h2>
                <p style="text-align: center; color: var(--text-light); margin-bottom: 40px;">Make your journey smoother and more enjoyable with our expert advice.</p>
                
                <div class="tips-grid">
                    <div class="tip-card">
                        <h3>Pack Smart, Travel Light</h3>
                        <p>Learn the art of minimalist packing to avoid extra baggage fees and enjoy greater mobility. Roll your clothes!</p>
                    </div>
                    <div class="tip-card">
                        <h3>Embrace Local Culture</h3>
                        <p>Step out of your comfort zone and try local cuisine, learn basic phrases, and respect local customs for an authentic experience.</p>
                    </div>
                    <div class="tip-card">
                        <h3>Stay Connected Safely</h3>
                        <p>Use a local SIM card or eSIM for affordable data. Always inform a family member about your itinerary and keep copies of documents.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact / Booking Section --><section id="contact" style="background-color: var(--bg-light);">
            <div class="container">
                <h2 class="section-title">Plan Your Dream Trip</h2>
                <p style="text-align: center; color: var(--text-light); margin-bottom: 40px;">Reach out to our travel experts for personalized packages and advice.</p>
                
                <form class="contact-form" onsubmit="handleBooking(event)">
                    <label for="name">Your Full Name:</label>
                    <input type="text" id="name" name="name" placeholder="E.g., Anjali Mehta" required>

                    <label for="email">Email Address:</label>
                    <input type="email" id="email" name="email" placeholder="E.g., anjali.m@example.com" required>

                    <label for="phone">Mobile Number:</label>
                    <input type="tel" id="phone" name="phone" pattern="[0-9]{10}" placeholder="E.g., 9876543210 (10 digits)" required>

                    <label for="destination">Preferred Destination:</label>
                    <select id="destination" name="destination">
                        <option value="">Any Destination</option>
                        <option value="Swiss Alps">Swiss Alps</option>
                        <option value="Thailand">Thailand</option>
                        <option value="Rajasthan">Rajasthan, India</option>
                        <option value="Paris">Paris, France</option>
                        <option value="Maldives">Maldives</option>
                        <option value="Kyoto">Kyoto, Japan</option>
                        <option value="Other">Other (Specify in message)</option>
                    </select>

                    <label for="message">Your Message / Requirements:</label>
                    <textarea id="message" name="message" placeholder="Tell us about your travel dreams, preferred dates, number of travelers, and any special requests." required></textarea>

                    <button type="submit" class="button primary">Send Inquiry</button>
                </form>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
                <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
                <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
            </div>
            <p>&copy; 2025 LuxeVoyage Travel Agency. All rights reserved.</p>
        </div>
    </footer>

    <!-- Font Awesome for Social Icons (Optional, but adds to professional look) --><script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>

    <script type="text/javascript">
        // Basic JavaScript for handling form submission (no backend for this example)
        function handleBooking(event) {
            event.preventDefault(); // Prevent actual form submission

            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const phone = document.getElementById('phone').value;
            const destination = document.getElementById('destination').value;
            const message = document.getElementById('message').value;

            // Simple validation (more robust validation would be done on backend)
            if (!name || !email || !phone || !message) {
                alert('Please fill in all required fields.');
                return;
            }
            if (!/^\d{10}$/.test(phone)) {
                 alert('Please enter a valid 10-digit Indian mobile number.');
                 return;
            }

            // Simulate sending data
            console.log('Booking Inquiry Submitted:');
            console.log('Name:', name);
            console.log('Email:', email);
            console.log('Phone:', phone);
            console.log('Destination:', destination);
            console.log('Message:', message);

            alert('Thank you, ' + name.split(' ')[0] + '! Your inquiry has been sent to LuxeVoyage. We will contact you shortly to plan your dream trip!');

            // Clear the form
            event.target.reset();
        }
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();

                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
