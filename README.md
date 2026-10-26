# -tiana-beauty-studio
    My first beauty business website
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tiana Beauty Studio</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f8f0e7;
            color: #4a3025;
        }

        header {
            background-color: #4a3025;
            color: #fff5e9;
            text-align: center;
            padding: 30px 15px;
        }

        header h1 {
            letter-spacing: 3px;
            margin-bottom: 10px;
        }

        nav {
            background-color: #e5d1bd;
            padding: 15px;
            text-align: center;
        }

        nav a {
            color: #4a3025;
            text-decoration: none;
            margin: 0 10px;
            font-weight: bold;
        }

        .hero {
            text-align: center;
            padding: 45px 20px;
        }

        .hero h2 {
            font-size: 30px;
        }

        .button {
            display: inline-block;
            background-color: #4a3025;
            color: white;
            padding: 13px 24px;
            text-decoration: none;
            border-radius: 25px;
            margin-top: 10px;
        }

        .services {
            padding: 30px 20px;
            text-align: center;
        }

        .card {
            background-color: #fffaf5;
            padding: 25px;
            margin: 15px auto;
            max-width: 350px;
            border-radius: 15px;
            box-shadow: 0 4px 12px #d8c5b5;
        }

        .card h3 {
            color: #80543e;
        }

        .booking {
            background-color: #e5d1bd;
            padding: 35px 20px;
            text-align: center;
        }

        input, select, textarea {
            display: block;
            width: 90%;
            max-width: 400px;
            margin: 12px auto;
            padding: 12px;
            border: 1px solid #c5aa94;
            border-radius: 8px;
            box-sizing: border-box;
            font-size: 16px;
        }

        button {
            background-color: #4a3025;
            color: white;
            padding: 14px 25px;
            border: none;
            border-radius: 25px;
            font-size: 16px;
        }

        footer {
            background-color: #4a3025;
            color: white;
            text-align: center;
            padding: 20px;
        }
    </style>
</head>

<body>

    <header>
        <h1>TIANA BEAUTY STUDIO</h1>
        <p>Beauty in Every Detail ✨</p>
    </header>

    <nav>
        <a href="#home">Home</a>
        <a href="#services">Services</a>
        <a href="#booking">Book Us</a>
    </nav>

    <section class="hero" id="home">
        <h2>Your Beauty, Our Passion 🤎</h2>
        <p>Enhancing your natural beauty, one lash at a time.</p>
        <a href="#booking" class="button">Book an Appointment</a>
    </section>

    <section class="services" id="services">
        <h2>Our Services</h2>
        <p>Simple elegance. Beautiful results.</p>

        <div class="card">
            <h3>Classic Lash Extensions</h3>
            <p>Soft, natural-looking lashes.</p>
            <p><strong>₦10,000</strong></p>
        </div>

        <div class="card">
            <h3>Volume Lash Extensions</h3>
            <p>Fuller lashes for a glamorous look.</p>
            <p><strong>₦15,000</strong></p>
        </div>

        <div class="card">
            <h3>Brow Shaping</h3>
            <p>Beautifully shaped and defined brows.</p>
            <p><strong>₦5,000</strong></p>
        </div>

        <div class="card">
            <h3>Lash Removal</h3>
            <p>Gentle removal of lash extensions.</p>
            <p><strong>₦3,000</strong></p>
        </div>
    </section>

    <section class="booking" id="booking">
        <h2>Book Your Appointment 📅</h2>
        <p>Fill in your details to prepare a booking request.</p>

        <form id="bookingForm">
            <input type="text" id="name"
                placeholder="Your full name" required>

            <input type="tel" id="phone"
                placeholder="Your phone number" required>

            <select id="service" required>
                <option value="">Choose a service</option>
                <option>Classic Lash Extensions</option>
                <option>Volume Lash Extensions</option>
                <option>Brow Shaping</option>
                <option>Lash Removal</option>
            </select>

            <input type="date" id="date" required>

            <textarea id="notes"
                placeholder="Additional details (optional)"
                rows="4"></textarea>

            <button type="submit">Prepare Booking</button>
        </form>

        <p id="message"></p>
    </section>

    <footer>
        <p>© 2026 Tiana Beauty Studio</p>
        <p>Beauty • Confidence • Elegance 🤎</p>
    </footer>

    <script>
        document.getElementById("bookingForm")
        .addEventListener("submit", function(event) {
            event.preventDefault();

            const name = document.getElementById("name").value;
            const phone = document.getElementById("phone").value;
            const service = document.getElementById("service").value;
            const date = document.getElementById("date").value;
            const notes = document.getElementById("notes").value;

            const message =
                "Hello Tiana Beauty Studio!%0A" +
                "My name is " + encodeURIComponent(name) + ".%0A" +
                "Phone: " + encodeURIComponent(phone) + "%0A" +
                "Service: " + encodeURIComponent(service) + "%0A" +
                "Preferred date: " + encodeURIComponent(date) + "%0A" +
                "Additional details: " + encodeURIComponent(notes);

            document.getElementById("message").innerHTML =
                "Your booking request is ready! " +
                '<a href="https://wa.me/?text=' + message +
                '" target="_blank">Continue on WhatsApp</a>';
        });
    </script>

</body>
</html>