<style>
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
      font-size: 14px; /* Font size for the links */
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
      font-size: 27px;
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
      font-size: 27px;
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

  /* New Text Section */
  .intro-text {
      text-align: center;
      padding: 40px;
      background-color: #f0f0f0; /* Light background for the text section */
  }

  .intro-text h2 {
      font-size: 24px;
      color: #0e194d;
  }

  .intro-text p {
      font-size: 14px;
      color: #0e194d;
  }

  /* Box Container */
  .box-container {
      display: grid;
      grid-template-columns: 1fr 1fr; /* Two columns for smaller boxes (Tarina and Palvelut) */
      gap: 10px;
      margin-top: 40px;
  }

  /* Make sure the boxes with background images (Palvelut and Koulutus) still stack vertically */
  .box-container .box-image {
      grid-column: span 2; /* These two boxes will span across both columns */
  }

  /* Box Styles */
  .box {
      background-color: #38B6FF;
      background-color: #0e194d;
      box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3), -2px -2px 5px rgba(92, 97, 102, 0.5);
      border: 1px solid #ddd;
      border-radius: 8px;
      text-align: center;
      padding: 20px; /* Increased padding */
      transition: transform 0.3s ease;
  }

  .box h3 {
      margin-bottom: 15px; /* Space between title and paragraph */
      font-size: 24px;
      text-shadow: 2px 2px 5px black; /* Horizontal shadow, vertical shadow, blur radius, color */
      color: #e1705d;
  }

  .box p {
      font-size: 14px;
      color: #e1705d;
  }

  .box:hover {
      transform: translateY(-10px);
  }

  /* Smaller Boxes with Reduced Width */
  .box-small {
      background-image: url('Pallot.jpg'); /* Corrected with url() */
      box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3), -2px -2px 5px rgba(92, 97, 102, 0.5);
      padding: 20px;
      height: 150px; /* Set a fixed height */
      border-radius: 8px;
      text-align: center;
      transition: transform 0.3s ease;
  }

  /* Box with Background Image */
  .box-image {
     background-image: url('Kuva24.jpg'); /* Corrected with url() */
      background-size: cover;
      background-position: center;
      color: #0e194d;
      padding: 40px;
      text-align: center;
      width: 100%; /* Set a fixed height */
      border-radius: 8px;
      box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3), -2px -2px 5px rgba(92, 97, 102, 0.5);
  }

  .box-image h3 {
      margin-bottom: 20px; /* Space between title and paragraph */
      font-size: 24px;
      color: #e1705d;
  }

  .box-image p {
      font-size: 14px;
      color: #e1705d;
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

  /* Pricing Section Styles */
  .pricing-section {
      background-color: #f9f9f9;
      padding: 40px 20px;
      text-align: center;
  }

  .pricing-title {
      font-size: 26px;
      color: #0e194d;
      margin-bottom: 30px;
  }

  .pricing-table-container {
      overflow-x: auto;
  }

  .pricing-table {
      width: 90%;
      max-width: 900px;
      margin: 0 auto;
      border-collapse: collapse;
      background-color: white;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.15);
      border-radius: 8px;
      overflow: hidden;
  }

  .pricing-table th,
  .pricing-table td {
      padding: 15px 20px;
      text-align: left;
      font-size: 14px;
      color: #0e194d;
  }

  .pricing-table thead {
      background-color: #e1705d;
      color: white;
  }

  .pricing-table tbody tr:nth-child(even) {
      background-color: #f2f2f2;
  }

  .pricing-table tbody tr:hover {
      background-color: #ffe5e0;
  }
</style>

<!-- Your existing HTML content... -->

<section>
  <div class="box-container">
    <!-- Existing boxes go here -->
  </div>

  <!-- Pricing Section -->
  <section class="pricing-section">
    <h2 class="pricing-title">Palveluiden hinnasto</h2>
    <div class="pricing-table-container">
      <table class="pricing-table">
        <thead>
          <tr>
            <th>Palvelu</th>
            <th>Kuvaus</th>
            <th>Hinta (alv 0%)</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Liiketoiminnan Konsultointi</td>
            <td>Yksilöllinen liiketoiminnan kehitysneuvonta</td>
            <td>€120 / h</td>
          </tr>
          <tr>
            <td>Strategiatyöpaja</td>
            <td>4 tunnin työpaja johdon ja tiimin kanssa</td>
            <td>€450 / työpaja</td>
          </tr>
          <tr>
            <td>Verkkokoulutus</td>
            <td>Itsenäisesti suoritettava koulutusmateriaali</td>
            <td>€89 / osallistuja</td>
          </tr>
          <tr>
            <td>Henkilökohtainen mentorointi</td>
            <td>1-on-1 mentorointi 60 min</td>
            <td>€95 / sessio</td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>
</section>
