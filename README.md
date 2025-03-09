<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Self-Help-You</title>
    <style>
        /* Reset default margin and padding */
        body, html {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        /* Styling the navigation bar */
        .navbar {
            background-color: #e1705d; /* Red background color */
            overflow: hidden; /* Ensures the content is contained within the navbar */
            text-align: center; /* Centers the links */
        }

        /* Styling each link inside the navbar */
        .navbar a {
            display: inline-block; /* Display links horizontally */
            padding: 14px 20px; /* Padding inside each link */
            text-decoration: none; /* Removes underline from links */
            color: white; /* White text color */
            font-size: 16px; /* Font size for the links */
            transition: background-color 0.3s ease; /* Smooth transition for background color change */
        }

        /* Hover effect for the links */
        .navbar a:hover {
            background-color: #ddd; /* Light background when hovered */
            color: black; /* Change text color when hovered */
        }

        /* Active link styling (when a link is clicked or active) */
        .navbar a.active {
            background-color: #0e194d; /* Blue background for active link */
            color: white; /* Keep text white for active link */
        }

        /* Hamburger menu icon styling */
        .navbar .icon {
            z-index: 2;
            display: none;
            font-size: 30px;
            color: white;
            padding: 14px 20px;
            background-color: #0e194d;
            cursor: pointer;
        }

        /* For small screens (mobile devices) */
        @media screen and (max-width: 768px) {
            .navbar a {
                display: none; /* Hide the links by default */
                width: 100%; /* Make the links take full width */
                text-align: left; /* Align links to the left */
                padding: 14px; /* Adjust padding for the links */
            }

            .navbar a.active {
                background-color: #0e194d;
                color: white;
            }

            /* Display the hamburger icon */
            .navbar .icon {
                display: block;
            }

            /* When the hamburger icon is clicked, show the links */
            .navbar.responsive a {
                display: block;
            }

            .navbar.responsive .icon {
                position: absolute;
                right: 0;
                top: 0;
            }
        }

        /* Styling for the header with rolling text effect */
        .header {
            background-color: #0e194d;
            color: white;
            padding: 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        /* Rolling text effect */
        .header h1 {
            display: inline-block;
            font-size: 36px;
            white-space: nowrap; /* Prevent the title from wrapping */
            animation: rollText 10s linear infinite; /* Apply animation to roll the text */
            position: relative;
            z-index: 2;
        }

        /* Keyframes for rolling text animation */
        @keyframes rollText {
            0% {
                transform: translateX(100%); /* Start off to the right */
            }
            100% {
                transform: translateX(-100%); /* End off to the left */
            }
        }

        /* Box Container */
        .box-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 10px;
            margin-top: 40px;
        }

        /* Box Styles */
        .box {
            background-color: #38B6FF;
            box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3), -2px -2px 5px rgba(92, 97, 102, 0.5);
            border: 1px solid #ddd;
            border-radius: 8px;
            text-align: center;
            padding: 20px;
            transition: transform 0.3s ease;
        }

        .box h3 {
            margin: 20px 0 10px;
            font-size: 1.2rem;
            color: #0e194d;
        }

        .box p {
            font-size: 1rem;
            color: #0e194d;
        }

        .box:hover {
            transform: translateY(-10px);
        }

        footer {
            text-align: center;
            padding: 20px;
            background-color: #0e194d; /* Blue background for the footer */
            color: white; /* White text color */
        }

        footer a {
            text-decoration: none; /* Removes underline */
            color: white; /* Link color in the footer */
            font-size: 16px; /* Optional: Adjust font size for links */
            margin: 0 10px; /* Add spacing between links */
            transition: color 0.3s ease; /* Smooth transition for color change */
        }

        footer a:hover {
            color: #FF5733; /* Color when hovered (e.g., light orange) */
        }

        footer a:visited {
            color: #8E44AD; /* Purple color after the link is visited */
        }

        /* Footer Bottom */
        .footer-bottom {
            padding-top: 10px;
        }

        /* Add space between the last box and footer */
        section {
            padding-bottom: 40px; /* Space between content and footer */
        }

    </style>
</head>
<body>

    <!-- Top Navigation Bar placed before the header -->
    <div class="navbar" id="myNavbar">
        <a href="#home" class="active">Koti</a>
        <a href="/Meista">Meistä</a>
        <a href="/Yritys">Yritys</a>
        <a href="#contact">Palvelut</a>
        <a href="#contact">Koulutus</a>
        <!-- Hamburger Icon -->
        <a href="javascript:void(0);" class="icon" onclick="toggleNavbar()">&#9776;</a>
    </div>

    <!-- Header with rolling text effect -->
    <div class="header">
        <h1>Self-Help-You</h1>
    </div>

    <!-- Main Content -->
    <section>
        <div class="box-container">
            <!-- Meistä Box -->
            <div class="box">
                <h3>Meistä</h3>
                <p>Lue lisää meistä ja referensseistämme.</p>
                <a href="/Meista" class="cta-btn">Lue lisää</a>
            </div>

            <!-- Yritys Box -->
            <div class="box">
                <h3>Yritys</h3>
                <p>Tutustu yritykseemme sekä henkilökuntaamme.</p>
                <a href="/Meista" class="cta-btn">Tutustu</a>
            </div>

            <!-- Palvelut Box -->
            <div class="box">
                <h3>Palvelut</h3>
                <p>Kuinka voimme auttaa Sinua ja yritystoimintaasi tulevaisuuden suunnittelussa.</p>
                <a href="/Meista" class="cta-btn">Katso tästä</a>
            </div>

            <!-- Koulutus Box -->
            <div class="box">
                <h3>Koulutus</h3>
                <p>Monipuoliset ja monimuotoiset koulutukset räätälöity Sinun yritystarpeillesi.</p>
                <a href="/Meista" class="cta-btn">Lue lisää</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-section contact">
            <h4>Self-Help-You</h4>
            <a href="/Otayhteytta" class="cta-btn">Ota yhteyttä</a>
            <a href="/Sahkoposti" class="cta-btn">Sähköposti</a>
            <a href="/Kanavat" class="cta-btn">Kanavat</a>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2025 Self-Help-You. Kaikki oikeudet pidätetään.</p>
        </div>
    </footer>

    <script>
        /* Function to toggle the navbar on small screens */
        function toggleNavbar() {
            var navbar = document.getElementById("myNavbar");
            navbar.classList.toggle("responsive");
        }
    </script>
</body>
</html>
