
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GlobeFares</title>
  <Style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #ffffff;
    }

    /* ------------ TOP NAVIGATION ------------ */
    .top-header {
      width: 100%;
      padding: 15px 40px;
      background: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    
    .logo .plane {
      width: 250px;
      margin-left: 5px;
    }

    .top-header nav {
      display: flex;
      align-items: center;
      gap: 25px;
    }

    nav a {
      text-decoration: none;
      color: #04074b
      font-size: 16px;
      font-weight: 550;
    }

    .flag {
      width: 28px;
    }

    /* ------------ BACKGROUND SLIDER ------------ */
   

    .hero {
  position: relative;
  min-height: 600px;   /* allows expansion */
  display: flex;
}

.bg-slide {
  flex: 1;
  height: 600px;       /* ensures scrolling height */
  background-size: cover;
  background-position: center;
}

.search-panel {
  position: relative;  /* remove absolute */
  margin-top: 120px;
  width: 85%;
  text-align: center;
  color: white;
}

    /* Images (replace with your originals if needed) */
    .img1 {
      background-image: url("eiffel.png");
    }

    .img2 {
      background-image: url("liberty.png");
    }

    .img3 {
      background-image: url("burjkhalifa.png");
    }

    .img4 {
      background-image: url("skylines.png");
    }

    .img5 {
      background-image: url("rome.png");
    }

    .img6 {
      background-image: url("kutubminar.png");
    }

    .img7 {
      background-image: url("londonbridge.png");
    }

    /* ------------ SEARCH PANEL ------------ */
    .search-panel {
      position: absolute;
      bottom: 40px;
      left: 50%;
      transform: translateX(-50%);
      width: 85%;
      text-align: center;
      color: white;
    }

    /* TOP TABS */
    .top-tabs button {
      background: rgba(0, 0, 0, 0.55);
      border: none;
      color: white;
      padding: 10px 20px;
      border-radius: 25px;
      margin: 150px 5px;
      font-size: 16px;
      cursor: pointer;
    }

    .top-tabs .active {
      background: rgba(50, 50, 80, 0.8);
    }

    /* TRIP TYPE */
    /* Keep all elements in one line */
.trip-type {
display: flex;
align-items: center;
gap: 10px;
}

/* Buttons styling stays same */
.trip-type button {
background: rgba(0, 0, 0, 0.55);
border: none;
color: white;
padding: 10px 22px;
border-radius: 25px;
cursor: pointer;
white-space: nowrap;
}
    .triptype-dropdown {
  position: relative;
  display: inline-block;
}

.triptype-btn {
  background: rgba(0,0,0,0.55);
  color: white;
  padding: 10px 16px;
  border-radius: 10px 10px 0 0;
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 16px;
}

.trip-icon {
  opacity: 0.8;
}

.arrow {
  font-size: 12px;
  margin-left: auto;
}

.triptype-menu {
  display: none;
  list-style: none;
  padding: 0;
  margin: 0;
  width: 220px;
  background: #2b2f36;
  border-radius: 0 0 12px 12px;
  overflow: hidden;
  position: absolute;
  top: 48px;
  left: 0;
  z-index: 9999;
}

.triptype-menu li {
  padding: 14px 18px;
  cursor: pointer;
  color: #ddd;
  font-size: 15px;
}

.triptype-menu li:hover {
  background: #363c47;
}

.triptype-menu li.active {
  background: #43506a;
  font-weight: 500;
}

.check {
  margin-right: 10px;
  opacity: 0.9;
}


   
    /* DROPDOWN */
    .cabin-dropdown {
      position: relative;
      /* anchor for dropdown */
    }

    .cabin-btn {
      background: rgba(0, 0, 0, 0.55);
      color: white;
      padding: 10px 22px;
      border-radius: 25px;
      border: none;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    /* Dropdown menu appears directly under button */
    .cabin-menu {
      position: absolute;
      top: 48px;
      /* 👈 aligns UNDER the Economy button */
      left: 0;
      width: 200px;
      background: #2b2f36;
      border-radius: 12px;
      padding: 0;
      list-style: none;
      display: none;
      z-index: 99999;
    }

    .cabin-menu li {
      padding: 12px;
      color: #e5e5e5;
      cursor: pointer;
    }

    .cabin-menu li.active {
      background: #3e4a63;
      color: white;
    }

    .cabin-menu li:hover {
      background: #4d5a78;
    }

    /* Checkmark spacing */
    .check {
      margin-right: 6px;
    }


    /* SEARCH FIELDS */
    .search-box {
      display: flex;
      justify-content: center;
      gap: 10px;
      margin-top: 15px;
    }

    .search-box input {
      width: 22%;
      padding: 12px;
      border-radius: 25px;
      border: none;
      outline: none;
      font-size: 15px;
    }

    .search-btn {
      width: 18%;
      padding: 12px;
      border-radius: 25px;
      border: none;
      font-size: 17px;
      background: #1a1f3a;
      color: white;
      cursor: pointer;
    }

    /* FILTERS */
    .filters {
      margin-top: 18px;
    }

    .filters button {
      background: rgba(0, 0, 0, 0.55);
      border: none;
      color: white;
      padding: 10px 18px;
      border-radius: 20px;
      margin: 4px;
      cursor: pointer;
    }

    .passenger-dropdown {
  position: relative;
  display: inline-block;
}

.passenger-btn {
  background: rgba(0,0,0,0.50);
  color: white;
  padding: 7px 13px;
  border-radius: 20px;
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 5px;
}

.passenger-menu {
  position: absolute;
  top: 45px;
  left: 0;
  width: 250px;
  padding: 10px;
  background: #2b2f36;
  border-radius: 15px;
  display: none;
  z-index: 9999;
}

.row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 0;
  border-bottom: 1px solid #3a3f4a;
}

.row:last-child {
  border-bottom: none;
}

.label {
  color: white;
  font-size: 16px;
}

.sub {
  color: #c6c6c6;
  font-size: 12px;
}

.counter {
  display: flex;
  align-items: center;
  gap: 10px;
}

.counter button {
  width: 30px;
  height: 30px;
  border-radius: 8px;
  border: none;
  background: #4a4f5a;
  color: white;
  font-size: 20px;
  cursor: pointer;
}

.counter span {
  width: 20px;
  text-align: center;
  color: white;
  font-size: 18px;
}

.actions {
  margin-top: 10px;
  display: flex;
  justify-content: space-between;
}

.actions button {
  background: none;
  border: none;
  color: #8bb1ff;
  font-size: 16px;
  cursor: pointer;
}

<!--WHY CHOOSE GLOBEFARES-->

/* SECTION WRAPPER */
.why-section {
    width: 100%;
    background: #000;
    padding: 60px 20px;
    display: flex;
    justify-content: center;
}

/* MAIN CONTAINER */
.why-globefares {
    max-width: 900px;
    width: 100%;
    text-align: center;
}

/* HEADING */
.heading {
    font-size: 32px;
    font-weight: 700;
    color: #ffffff;
    margin-bottom: 25px;
    letter-spacing: 1px;
}

/* BENEFITS LIST */
.why-box {
    display: flex;
    flex-direction: column;
    gap: 15px;
}

.why-box span {
    background: #111827;
    padding: 14px 20px;
    border-radius: 10px;
    font-size: 18px;
    color: #e5e5e5;
    border: 1px solid #2b2f36;
    text-align: center;
    transition: 0.3s ease;
}

/* Hover effect */
.why-box span:hover {
    background: #1f2937;
    transform: translateY(-2px);
}

.features-section {
      display: flex;
      justify-content: space-around;
      align-items: flex-start;
      background: #fff;
      padding: 40px 0;
    }
    .feature-box {
      text-align: center;
      width: 220px;
    }
    .feature-icon {
      font-size: 56px;
      margin-bottom: 20px;
      color: #04074b;
      display: block;
    }
    .feature-title {
      font-size: 20px;
      font-weight: 550;
      margin: 0;
      color: #04074b
    }
    
    /* AIRLINES & TRAVEL PARTNERS SECTION */

    .section-container {
      max-width: 1200px;
      margin: 40px auto;
      padding: 0 16px;
      font-family: Arial, sans-serif;
    }
    .section-row {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      margin-bottom: 32px;
    }
    .section-info {
      flex-basis: 23%;
      min-width: 250px;
    }
    .section-info h2 {
      font-size: 2rem;
      margin-bottom: 10px;
      color: #222;
    }
    .section-info p {
      color: #444;
      margin-top: 0;
      font-size: 1.1rem;
    }
    .logos-grid {
      flex-basis: 75%;
      display: flex;
      flex-wrap: wrap;
      gap: 32px 42px;
      align-items: center;
      justify-content: flex-start;
    }
    .logo-item {
      flex: 0 0 130px;
      margin-bottom: 22px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .logo-item img {
      max-width: 120px;
      max-height: 40px;
      object-fit: contain;
      filter: drop-shadow(0 2px 8px rgba(0,0,0,0.05));
    }
    @media (max-width: 900px) {
      .section-row {
        flex-direction: column;
      }
      .logos-grid {
        justify-content: flex-start;
      }
    }

    /* FLIGHT TO TOP CITIES AND COUNTRY FOR UNITED STATE */

    .dest-section {
      max-width: 1100px;
      margin: 45px auto;
      font-family: Arial, sans-serif;
      color: #222;
      padding: 0 16px;
    }
    .dest-title {
      font-weight: 700;
      font-size: 1.1rem;
      margin-bottom: 5px;
      margin-top: 32px;
    }
    .dest-list-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 0 44px;
    }
    .dest-col {
      flex: 1 1 220px;
      min-width: 170px;
      margin-bottom: 12px;
    }
    .dest-link {
      display: block;
      margin-bottom: 8px;
      color: #222;
      text-decoration: none;
      font-size: 1rem;
      transition: color 0.2s;
    }
    .dest-link:hover {
      color: #1e88e5;
      text-decoration: underline;
    }
    @media (max-width: 800px) {
      .dest-list-grid {
        flex-direction: column;
        gap: 0;
      }
      .dest-col {
        min-width: 100%;
      }
    }
    /* FOOTER LINKS */

    .site-footer {
      background: #191919;
      color: #fff;
      padding: 50px 0 16px;
      font-family: Arial, sans-serif;
    }
    .footer-main {
      max-width: 1200px;
      margin: 0 auto 18px auto;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      padding: 0 32px;
    }
    .footer-col {
      min-width: 180px;
      margin-bottom: 22px;
    }
    .footer-title {
      font-weight: bold;
      font-size: 1.1rem;
      margin-bottom: 16px;
      letter-spacing: 0.5px;
    }
    .footer-list {
      padding: 0;
      margin: 0;
      list-style: none;
    }
    .footer-list li {
      margin-bottom: 11px;
    }
    .footer-list a {
      color: #fff;
      text-decoration: none;
      font-size: 1rem;
      transition: color 0.2s;
    }
    .footer-list a:hover {
      color: #35C047;
      text-decoration: underline;
    }
    .footer-badge {
      background: #ff8717;
      color: #fff;
      border-radius: 5px;
      padding: 2px 9px;
      font-size: 0.88em;
      margin-left: 7px;
      vertical-align: middle;
    }
    .footer-bottom {
      max-width: 1200px;
      margin: 0 auto;
      padding: 23px 32px 0 32px;
      font-size: 1rem;
      border-top: 1px solid #333;
      color: #dedede;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .footer-social {
      display: flex;
      align-items: center;
      gap: 15px;
    }
    .footer-social a {
      color: #fff;
      font-size: 1.25rem;
      transition: color 0.2s;
      text-decoration: none;
    }
    .footer-social a:hover {
      color: #35C047;
    }
    @media (max-width: 900px) {
      .footer-main {
        flex-direction: column;
        padding: 0 18px;
      }
      .footer-col {
        margin-bottom: 35px;
      }
      .footer-bottom {
        flex-direction: column;
        padding: 20px 18px 0 18px;
        align-items: flex-start;
        gap: 10px;
      }
    }


    
  </Style>

</head>

<body>

  <!-- TOP BAR -->
  <header class="top-header">
    <div class="logo">
      <img src="globefares logo.png" class="plane">
      
    </div>

    <nav>
      <img src="https://flagcdn.com/w20/us.png" class="flag">
      <a href="#">EN</a>
      <a href="#">USD</a>
      <a href="#">SUPPORT</a>
      <a href="#">LOGIN</a>
    </nav>
  </header>


  <!-- HERO BACKGROUND -->
  <section class="hero">
    <div class="bg-slide img1"></div>
    <div class="bg-slide img2"></div>
    <div class="bg-slide img3"></div>
    <div class="bg-slide img4"></div>
    <div class="bg-slide img5"></div>
    <div class="bg-slide img6"></div>
    <div class="bg-slide img7"></div>

    <!-- SEARCH PANEL -->
    <div class="search-panel">

      <!-- TABS -->
      <div class="top-tabs">
        <button class="active"><span>✈</span> Flights</button>
        <button><span>🏨</span> Hotels</button>
        <button><span>🚗</span> Cars</button>
      </div>

      <!-- TRIP TYPE -->


      <div class="trip-type">
        <div class="triptype-dropdown">
  <button class="triptype-btn" id="tripBtn">
    <span class="trip-icon">⇄</span>
    <span id="tripSelected">Round trip</span>
    <span class="arrow">▲</span>
  </button>

  <ul class="triptype-menu" id="tripMenu">
    <li class="active"><span class="check"></span> Round trip</li>
    <li>One way</li>
    <li>Multi-city</li>
  </ul>
</div>

        

        <div class="cabin-dropdown">
          <button class="cabin-btn" id="cabinBtn">
            <span id="cabinSelected">Economy</span>
            <span class="arrow">▲</span>
          </button>

          <ul class="cabin-menu" id="cabinMenu">
            <li class="active"><span class="check"></span> Economy</li>
            <li>Premium economy</li>
            <li>Business</li>
            <li>First</li>
          </ul>
        </div>

        <div class="passenger-dropdown">
  <button class="passenger-btn" id="passengerBtn">
    👤 <span id="passengerCount">1 Passenger</span>
    <span class="arrow">▲</span>
  </button>

  <div class="passenger-menu" id="passengerMenu">
    
    <!-- ADULTS -->
    <div class="row">
      <div class="label">
        Adults<br><span class="sub">Aged 12+</span>
      </div>
      <div class="counter">
        <button class="minus" onclick="changeCount('adults', -1)">−</button>
        <span id="adults">1</span>
        <button class="plus" onclick="changeCount('adults', 1)">+</button>
      </div>
    </div>

    <!-- CHILDREN -->
    <div class="row">
      <div class="label">
        Children<br><span class="sub">Aged 2–11</span>
      </div>
      <div class="counter">
        <button class="minus" onclick="changeCount('children', -1)">−</button>
        <span id="children">0</span>
        <button class="plus" onclick="changeCount('children', 1)">+</button>
      </div>
    </div>

    <!-- INFANTS SEAT -->
    <div class="row">
      <div class="label">
        Infants<br><span class="sub">In seat</span>
      </div>
      <div class="counter">
        <button class="minus" onclick="changeCount('infantSeat', -1)">−</button>
        <span id="infantSeat">0</span>
        <button class="plus" onclick="changeCount('infantSeat', 1)">+</button>
      </div>
    </div>

    <!-- INFANTS LAP -->
    <div class="row">
      <div class="label">
        Infants<br><span class="sub">On lap</span>
      </div>
      <div class="counter">
        <button class="minus" onclick="changeCount('infantLap', -1)">−</button>
        <span id="infantLap">0</span>
        <button class="plus" onclick="changeCount('infantLap', 1)">+</button>
      </div>
    </div>

    <div class="actions">
      <button class="cancel" onclick="closePassengers()">Cancel</button>
      <button class="done" onclick="closePassengers()">Done</button>
    </div>
  </div>
</div>


      </div>




      <!-- SEARCH FIELDS -->
      <div class="search-box">
        <input type="text" placeholder="Departure,City,Airport...">
        <input type="text" placeholder="Destination,City,Airport...">
        <input type="date" placeholder="Depart date">
        <input type="date" placeholder="Return date">
        <button class="search-btn">Search</button>
      </div>

      <!-- BOTTOM FILTERS -->
      <div class="filters">
        <button>Nearby airports</button>
        <button>Direct Flight</button>
        <button>Connecting-Airports</button>
        <button>Airlines</button>
         <button>Date grid</button>
        <button>Price grid</button>
      </div>

    </div>

    
  </section>

  <section>
    <div class="features-section">
  <div class="feature-box">
    <!-- Replace with your image or SVG icon -->
    <span class="feature-icon">✈️</span>
    <p class="feature-title">Best Travel Deals in the World</p>
  </div>
  <div class="feature-box">
    <span class="feature-icon">🔍</span>
    <p class="feature-title">Thousands of Flights & Hotel Deals</p>
  </div>
  <div class="feature-box">
    <span class="feature-icon">💳</span>
    <p class="feature-title">Multiple Payment Methods</p>
  </div>
  <div class="feature-box">
    <span class="feature-icon">📞</span>
    <p class="feature-title">24/7 Customer Service Support</p>
  </div>
</div>

</section>
 <div class="section-container">
    <!-- Airlines Section -->
    <div class="section-row">
      <div class="section-info">
        <h2>Popular Airlines in USA</h2>
        <p>Book cheap flights on your favorite US airlines</p>
      </div>
      <div class="logos-grid">
        <div class="logo-item"><img src="https://1000logos.net/wp-content/uploads/2021/05/American-Airlines-logo.png" alt="American Airlines"></div>
        <div class="logo-item"><img src="https://1000logos.net/wp-content/uploads/2017/03/Delta-Logo-1995.png" alt="Delta"></div>
        <div class="logo-item"><img src="https://1000logos.net/wp-content/uploads/2017/03/United-Airlines-Logo-2010.png" alt="United Airlines"></div>
        <div class="logo-item"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/28/Southwest_Airlines_logo_2014.svg/512px-Southwest_Airlines_logo_2014.svg.png" alt="Southwest Airlines"></div>
        <div class="logo-item"><img src="https://1000logos.net/wp-content/uploads/2017/05/Alaska-Airlines-Logo-768x432.png" alt="Alaska Airlines"></div>
        <div class="logo-item"><img src="https://upload.wikimedia.org/wikipedia/commons/9/9a/JetBlue_Airways_Logo.svg" alt="JetBlue"></div>
      </div>
    </div>

    <!-- Travel Partners Section -->
    <div class="section-row">
      <div class="section-info">
        <h2>Our Travel Partners</h2>
        <p>We search for the best deals on these top sites in the USA</p>
      </div>
      <div class="logos-grid">
        <div class="logo-item"><img src="https://upload.wikimedia.org/wikipedia/commons/6/6e/Expedia_Logo.svg" alt="Expedia"></div>
        <div class="logo-item"><img src="https://1000logos.net/wp-content/uploads/2017/06/Booking.com-logo.png" alt="Booking.com"></div>
        <div class="logo-item"><img src="https://upload.wikimedia.org/wikipedia/commons/4/44/Travelocity_Logo.svg" alt="Travelocity"></div>
        <div class="logo-item"><img src="https://1000logos.net/wp-content/uploads/2021/02/Orbitz-Logo-2018.png" alt="Orbitz"></div>
        <div class="logo-item"><img src="https://1000logos.net/wp-content/uploads/2017/05/Priceline-Logo.png" alt="Priceline"></div>
        <div class="logo-item"><img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/Hotwire_Logo.svg" alt="Hotwire"></div>
        <div class="logo-item"><img src="https://1000logos.net/wp-content/uploads/2021/05/KAYAK-logo.png" alt="Kayak"></div>
      </div>
    </div>
  </div>

<section>

</section>
<!--FLIGHT TO TOP CITIES AND COUNTRY FOR UNITED STATE-->
<section>
    <div class="dest-section">
    <div class="dest-title">Flights To Top Cities from The United States</div>
    <div class="dest-list-grid">
      <div class="dest-col">
        <a href="#" class="dest-link">Flights to New York City</a>
        <a href="#" class="dest-link">Flights to Washington</a>
        <a href="#" class="dest-link">Flights to Orlando</a>
      </div>
      <div class="dest-col">
        <a href="#" class="dest-link">Flights to Los Angeles</a>
        <a href="#" class="dest-link">Flights to San Francisco</a>
        <a href="#" class="dest-link">Flights to Houston</a>
      </div>
      <div class="dest-col">
        <a href="#" class="dest-link">Flights to Chicago</a>
        <a href="#" class="dest-link">Flights to Las Vegas</a>
      </div>
      <div class="dest-col">
        <a href="#" class="dest-link">Flights to Miami</a>
        <a href="#" class="dest-link">Flights to Dallas</a>
      </div>
    </div>

    <div class="dest-title">Flights To Top Countries from The United States</div>
    <div class="dest-list-grid">
      <div class="dest-col">
        <a href="#" class="dest-link">Flights to India</a>
        <a href="#" class="dest-link">Flights to United Arab Emirates</a>
        <a href="#" class="dest-link">Flights to Kuwait</a>
      </div>
      <div class="dest-col">
        <a href="#" class="dest-link">Flights to Egypt</a>
        <a href="#" class="dest-link">Flights to Canada</a>
        <a href="#" class="dest-link">Flights to Turkey</a>
      </div>
      <div class="dest-col">
        <a href="#" class="dest-link">Flights to Saudi Arabia</a>
        <a href="#" class="dest-link">Flights to Pakistan</a>
      </div>
      <div class="dest-col">
        <a href="#" class="dest-link">Flights to Jordan</a>
        <a href="#" class="dest-link">Flights to Iraq</a>
      </div>
    </div>
  </div>
</section>
<!--FOOTER LINKS & INFORMATION-->
<section>
    <footer class="site-footer">
    <div class="footer-main">
      <div class="footer-col">
        <div class="footer-title">COMPANY</div>
        <ul class="footer-list">
          <li><a href="#">About Globefares</a></li>
          <li><a href="#">Contact Us</a></li>
          <li><a href="#">Data Privacy Policy</a></li>
          <li><a href="#">Terms</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <div>
        Copyright ©2025 Globefares Pte Ltd. All Rights Reserved<br>
        
      </div>
      <div class="footer-social">
        <a href="#" aria-label="Facebook"></a>
        <a href="#" aria-label="X">✖</a>
        <a href="#" aria-label="Instagram">◉</a>
        <a href="#" aria-label="LinkedIn">⧫</a>
        <!-- Replace with SVG or icons in production -->
      </div>
    </div>
  </footer>
</section>


    



  <script>

    // CLASS DROPDOWN

    const btn = document.getElementById("cabinBtn");
    const menu = document.getElementById("cabinMenu");
    const selectedText = document.getElementById("cabinSelected");

    btn.addEventListener("click", () => {
      menu.style.display = menu.style.display === "block" ? "none" : "block";
    });

    // Update selected option
    document.querySelectorAll(".cabin-menu li").forEach(item => {
      item.addEventListener("click", () => {
        document.querySelector(".cabin-menu .active")?.classList.remove("active");
        item.classList.add("active");

        selectedText.textContent = item.textContent.trim();
        menu.style.display = "none";
      });
    });

    // PASSENGERS TYPE

   let maxPassengers = 9;

// Set default values on load
document.getElementById("adults").innerText = 1;
document.getElementById("children").innerText = 0;
document.getElementById("infantSeat").innerText = 0;
document.getElementById("infantLap").innerText = 0;

// ≈≈≈ FUNCTION: Total passengers
function totalPassengers() {
  return (
    Number(document.getElementById("adults").innerText) +
    Number(document.getElementById("children").innerText) +
    Number(document.getElementById("infantSeat").innerText) +
    Number(document.getElementById("infantLap").innerText)
  );
}

// ≈≈≈ FUNCTION: Update top label
function updatePassengerLabel() {
  let total = totalPassengers();
  document.getElementById("passengerCount").innerText =
    total + (total > 1 ? " Passengers" : " Passenger");
}

// Set label on page load
updatePassengerLabel();

// ≈≈≈ FUNCTION: Change counts
function changeCount(type, value) {
  let el = document.getElementById(type);
  let current = Number(el.innerText);

  // prevent negative
  if (current + value < 0) return;

  // prevent exceeding limit
  if (value === 1 && totalPassengers() >= maxPassengers) return;

  el.innerText = current + value;
  updatePassengerLabel();
}

// ≈≈≈ OPEN PASSENGER DROPDOWN
document.getElementById("passengerBtn").onclick = () => {
  document.getElementById("passengerMenu").style.display = "block";
};

// ≈≈≈ CLOSE PASSENGER DROPDOWN
function closePassengers() {
  document.getElementById("passengerMenu").style.display = "none";
}

// TRIP TYPE

const tripBtn = document.getElementById("tripBtn");
const tripMenu = document.getElementById("tripMenu");
const tripSelected = document.getElementById("tripSelected");

tripBtn.onclick = () => {
  tripMenu.style.display =
    tripMenu.style.display === "block" ? "none" : "block";
};

document.querySelectorAll(".triptype-menu li").forEach((item) => {
  item.addEventListener("click", () => {
    document
      .querySelector(".triptype-menu li.active")
      ?.classList.remove("active");

    item.classList.add("active");
    tripSelected.textContent = item.textContent.replace("✔", "").trim();
    tripMenu.style.display = "none";
  });
});

document.addEventListener("click", (e) => {
  if (!tripBtn.contains(e.target) && !tripMenu.contains(e.target)) {
    tripMenu.style.display = "none";
  }
});







  </script>



</body>

</html>
