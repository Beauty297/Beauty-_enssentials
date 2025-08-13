no<form action="https://formspree.io/f/moqkrgwp" method="POST">
    <div class="form-group">
        <label for="name">Your Name</label>
        <input type="text" id="name" name="name" required>
    </div>
    <div class="form-group">
        <label for="email">Email Address</label>
        <input type="email" id="email" name="email" required>
    </div>
    <div class="form-group">
        <label for="message">Message</label>
        <textarea id="message" name="message" rows="5" required></textarea>
    </div>
    <button type="submit" class="cta-button">Send Message</button>
</for index.html`, `git commit -m "Update contact form to use Formspree sample endpoint"`, and `git push`.

5. **Visit your site:**  
   - [https://beauty297.github.io/beauty_enssentials/](https://beauty297.github.io/beauty_enssentials/)
   
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beauty Essentials - Premium Beauty Tools & Pet Care</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #ffeef7 0%, #f8e8ff 100%);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #ff6b9d 0%, #c44569 100%);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 4px 20px rgba(255, 107, 157, 0.3);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            text-decoration: none;
            color: white;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 2rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            padding: 0.5rem 1rem;
            border-radius: 25px;
        }

        nav a:hover {
            background: rgba(255,255,255,0.2);
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 5rem 0;
            text-align: center;
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
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="20" cy="20" r="2" fill="rgba(255,255,255,0.1)"/><circle cx="80" cy="80" r="2" fill="rgba(255,255,255,0.1)"/><circle cx="40" cy="60" r="1" fill="rgba(255,255,255,0.1)"/></svg>');
            animation: float 20s infinite linear;
        }

        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); }
            100% { transform: translateY(-100px) rotate(360deg); }
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            background: linear-gradient(135deg, #ff6b9d 0%, #c44569 100%);
            color: white;
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            box-shadow: 0 8px 25px rgba(255, 107, 157, 0.4);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 35px rgba(255, 107, 157, 0.6);
        }

        /* Featured Products */
        .featured-products {
            padding: 5rem 0;
            background: white;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 100px;
            height: 4px;
            background: linear-gradient(135deg, #ff6b9d 0%, #c44569 100%);
            margin: 1rem auto;
            border-radius: 2px;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background: white;
            border-radius: 20px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            border: 1px solid #f0f0f0;
            position: relative;
            overflow: hidden;
        }

        .product-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
            transition: all 0.5s ease;
        }

        .product-card:hover::before {
            left: 100%;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .product-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            display: block;
        }

        .product-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #333;
        }

        .product-card p {
            color: #666;
            margin-bottom: 1.5rem;
        }

        .price {
            font-size: 1.5rem;
            font-weight: bold;
            color: #ff6b9d;
            margin-bottom: 1rem;
        }

        .buy-button {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 0.8rem 1.5rem;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .buy-button:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        /* About Section */
        .about {
            padding: 5rem 0;
            background: linear-gradient(135deg, #ffeef7 0%, #f8e8ff 100%);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: #333;
        }

        .about-text p {
            font-size: 1.1rem;
            color: #666;
            margin-bottom: 1.5rem;
        }

        .about-features {
            list-style: none;
        }

        .about-features li {
            padding: 0.5rem 0;
            color: #555;
            position: relative;
            padding-left: 2rem;
        }

        .about-features li::before {
            content: '✨';
            position: absolute;
            left: 0;
            color: #ff6b9d;
        }

        .about-image {
            background: linear-gradient(135deg, #ff6b9d 0%, #c44569 100%);
            border-radius: 20px;
            height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 4rem;
            box-shadow: 0 20px 40px rgba(255, 107, 157, 0.3);
        }

        /* Contact Section */
        .contact {
            padding: 5rem 0;
            background: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .contact-form {
            background: #f9f9f9;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #333;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #ff6b9d;
            box-shadow: 0 0 0 3px rgba(255, 107, 157, 0.1);
        }

        .contact-info h3 {
            margin-bottom: 2rem;
            color: #333;
            font-size: 1.8rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
            padding: 1rem;
            background: #f9f9f9;
            border-radius: 10px;
        }

        .contact-item-icon {
            font-size: 1.5rem;
            margin-right: 1rem;
            color: #ff6b9d;
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);
            color: white;
            text-align: center;
            padding: 3rem 0;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            margin-bottom: 1rem;
            color: #ff6b9d;
        }

        .footer-section p,
        .footer-section a {
            color: #bdc3c7;
            text-decoration: none;
            line-height: 1.8;
        }

        .footer-section a:hover {
            color: #ff6b9d;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 2rem;
        }


