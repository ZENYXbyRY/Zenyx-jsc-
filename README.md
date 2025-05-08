<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ZENYX JERSEYS - Premium Football Jerseys</title>
  <style>
    :root {
      --primary: #ff0000;
      --secondary: #000000;
      --light: #ffffff;
      --dark: #222222;
      --gray: #f5f5f5;
      --success: #28a745;
    }
    
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--light);
      color: var(--dark);
      line-height: 1.6;
    }
    
    /* Auth Modals */
    .auth-modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.7);
      z-index: 1000;
      justify-content: center;
      align-items: center;
    }
    
    .auth-content {
      background: var(--light);
      padding: 2rem;
      border-radius: 8px;
      width: 90%;
      max-width: 400px;
      position: relative;
      animation: modalFadeIn 0.3s;
    }
    
    @keyframes modalFadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    .close-auth {
      position: absolute;
      top: 1rem;
      right: 1rem;
      font-size: 1.5rem;
      cursor: pointer;
      color: var(--dark);
    }
    
    .auth-tabs {
      display: flex;
      margin-bottom: 1.5rem;
      border-bottom: 1px solid #ddd;
    }
    
    .auth-tab {
      padding: 0.5rem 1rem;
      cursor: pointer;
      flex: 1;
      text-align: center;
      transition: all 0.3s;
    }
    
    .auth-tab.active {
      border-bottom: 2px solid var(--primary);
      font-weight: bold;
      color: var(--primary);
    }
    
    .auth-form {
      display: none;
    }
    
    .auth-form.active {
      display: block;
    }
    
    .form-group {
      margin-bottom: 1rem;
    }
    
    .form-group label {
      display: block;
      margin-bottom: 0.5rem;
      font-weight: 500;
    }
    
    .form-group input, .form-group textarea, .form-group select {
      width: 100%;
      padding: 0.8rem;
      border: 1px solid #ddd;
      border-radius: 4px;
      font-family: inherit;
    }
    
    .auth-btn {
      width: 100%;
      padding: 0.8rem;
      background: var(--primary);
      color: var(--light);
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-weight: bold;
      margin-top: 1rem;
      transition: background 0.3s;
    }
    
    .auth-btn:hover {
      background: #cc0000;
    }
    
    /* Header Styles */
    header {
      background: var(--secondary);
      color: var(--light);
      padding: 1rem 0;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    }
    
    .header-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }
    
    .logo {
      font-size: 1.8rem;
      font-weight: bold;
      color: var(--light);
      text-decoration: none;
      display: flex;
      align-items: center;
    }
    
    .logo img {
      height: 40px;
      margin-right: 10px;
    }
    
    .logo span {
      color: var(--primary);
    }
    
    nav ul {
      display: flex;
      list-style: none;
      align-items: center;
    }
    
    nav ul li {
      margin-left: 1.5rem;
    }
    
    nav ul li a {
      color: var(--light);
      text-decoration: none;
      font-weight: 500;
      transition: color 0.3s;
    }
    
    nav ul li a:hover {
      color: var(--primary);
    }
    
    .auth-link {
      cursor: pointer;
    }
    
    .user-profile {
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }
    
    .user-avatar {
      width: 30px;
      height: 30px;
      border-radius: 50%;
      background: var(--primary);
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      color: white;
    }
    
    .cart-icon {
      position: relative;
    }
    
    .cart-count {
      position: absolute;
      top: -8px;
      right: -8px;
      background: var(--primary);
      color: white;
      border-radius: 50%;
      width: 20px;
      height: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.7rem;
    }
    
    /* Hero Section */
    .hero {
      background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1574629810360-7efbbe195018?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
      background-size: cover;
      background-position: center;
      height: 60vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: var(--light);
    }
    
    .hero-content {
      max-width: 800px;
      padding: 0 20px;
    }
    
    .hero h1 {
      font-size: 3rem;
      margin-bottom: 1rem;
    }
    
    .hero p {
      font-size: 1.2rem;
      margin-bottom: 2rem;
    }
    
    .btn {
      display: inline-block;
      background: var(--primary);
      color: var(--light);
      padding: 0.8rem 1.8rem;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      text-decoration: none;
      font-weight: bold;
      transition: background 0.3s;
    }
    
    .btn:hover {
      background: #cc0000;
    }
    
    /* Main Content */
    .container {
      max-width: 1200px;
      margin: 2rem auto;
      padding: 0 20px;
    }
    
    .section-title {
      text-align: center;
      margin-bottom: 2rem;
      font-size: 2rem;
      position: relative;
    }
    
    .section-title::after {
      content: '';
      display: block;
      width: 80px;
      height: 4px;
      background: var(--primary);
      margin: 0.5rem auto;
    }
    
    /* Search Bar */
    .search-bar {
      text-align: center;
      margin: 2rem 0;
    }
    
    .search-bar input {
      padding: 12px 20px;
      width: 100%;
      max-width: 500px;
      font-size: 1rem;
      border: 2px solid var(--secondary);
      border-radius: 30px;
      outline: none;
    }
    
    /* Jersey Grid */
    .jersey-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 2rem;
      margin: 2rem 0;
    }
    
    .jersey-card {
      background: var(--light);
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s, box-shadow 0.3s;
      border: 1px solid #eee;
    }
    
    .jersey-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
    }
    
    .jersey-img {
      width: 100%;
      height: 250px;
      object-fit: cover;
      transition: transform 0.3s;
    }
    
    .jersey-card:hover .jersey-img {
      transform: scale(1.05);
    }
    
    .jersey-info {
      padding: 1.5rem;
    }
    
    .jersey-title {
      font-size: 1.2rem;
      margin-bottom: 0.5rem;
    }
    
    .jersey-team {
      color: #666;
      margin-bottom: 0.5rem;
      font-size: 0.9rem;
    }
    
    .jersey-price {
      font-weight: bold;
      color: var(--primary);
      font-size: 1.2rem;
      margin-bottom: 1rem;
    }
    
    .size-select {
      width: 100%;
      padding: 8px;
      margin-bottom: 1rem;
      border: 1px solid #ddd;
      border-radius: 4px;
    }
    
    .add-to-cart {
      width: 100%;
      background: var(--secondary);
      color: var(--light);
      border: none;
      padding: 10px;
      border-radius: 4px;
      cursor: pointer;
      font-weight: bold;
      transition: background 0.3s;
    }
    
    .add-to-cart:hover {
      background: var(--primary);
    }
    
    /* Cart Modal */
    .modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5);
      z-index: 1000;
      overflow-y: auto;
    }
    
    .modal-content {
      background: var(--light);
      max-width: 800px;
      margin: 2rem auto;
      padding: 2rem;
      border-radius: 8px;
      position: relative;
      animation: modalFadeIn 0.3s;
    }
    
    .close-modal {
      position: absolute;
      top: 1rem;
      right: 1rem;
      font-size: 1.5rem;
      cursor: pointer;
      color: var(--dark);
    }
    
    .cart-items {
      margin: 1.5rem 0;
    }
    
    .cart-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 0;
      border-bottom: 1px solid #eee;
    }
    
    .cart-item-img {
      width: 80px;
      height: 80px;
      object-fit: cover;
      border-radius: 4px;
    }
    
    .cart-item-details {
      flex: 1;
      padding: 0 1rem;
    }
    
    .cart-item-title {
      font-weight: bold;
    }
    
    .cart-item-price {
      color: var(--primary);
      font-weight: bold;
    }
    
    .remove-item {
      color: #ff0000;
      cursor: pointer;
      background: none;
      border: none;
      font-size: 1.2rem;
    }
    
    .cart-total {
      text-align: right;
      font-size: 1.2rem;
      font-weight: bold;
      margin: 1rem 0;
    }
    
    .checkout-btn {
      width: 100%;
      padding: 12px;
      background: var(--primary);
      color: var(--light);
      border: none;
      border-radius: 4px;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s;
    }
    
    .checkout-btn:hover {
      background: #cc0000;
    }
    
    /* Checkout Form */
    .checkout-form {
      margin-top: 2rem;
    }
    
    .form-row {
      display: flex;
      gap: 1rem;
      margin-bottom: 1rem;
    }
    
    .form-row .form-group {
      flex: 1;
    }
    
    /* Payment Section */
    .payment-section {
      margin: 2rem 0;
      padding: 2rem;
      background: var(--gray);
      border-radius: 8px;
    }
    
    .payment-methods {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      margin: 1rem 0;
    }
    
    .payment-method {
      flex: 1;
      min-width: 200px;
      padding: 1rem;
      border: 1px solid #ddd;
      border-radius: 8px;
      text-align: center;
    }
    
    .payment-method img {
      height: 40px;
      margin-bottom: 0.5rem;
    }
    
    .qr-code {
      width: 200px;
      height: 200px;
      margin: 1rem auto;
      background: var(--light);
      padding: 1rem;
      border-radius: 8px;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    
    .qr-code img {
      max-width: 100%;
      max-height: 100%;
    }
    
    .upi-id {
      background: var(--light);
      padding: 1rem;
      border-radius: 8px;
      margin: 1rem 0;
      text-align: center;
      font-weight: bold;
    }
    
    .order-confirmation {
      text-align: center;
      padding: 2rem;
    }
    
    .order-confirmation h2 {
      color: var(--success);
      margin-bottom: 1rem;
    }
    
    .order-confirmation p {
      margin-bottom: 1rem;
    }
    
    .order-details {
      background: var(--gray);
      padding: 1.5rem;
      border-radius: 8px;
      margin: 1rem 0;
      text-align: left;
    }
    
    .order-details h3 {
      margin-bottom: 1rem;
    }
    
    /* Toast Notification */
    .toast {
      position: fixed;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      background: var(--primary);
      color: white;
      padding: 12px 24px;
      border-radius: 4px;
      box-shadow: 0 3px 10px rgba(0,0,0,0.2);
      z-index: 1000;
      animation: fadeInOut 3s ease-in-out;
      opacity: 0;
    }
    
    @keyframes fadeInOut {
      0% { opacity: 0; transform: translateX(-50%) translateY(20px); }
      10% { opacity: 1; transform: translateX(-50%) translateY(0); }
      90% { opacity: 1; transform: translateX(-50%) translateY(0); }
      100% { opacity: 0; transform: translateX(-50%) translateY(20px); }
    }
    
    /* Footer */
    footer {
      background: var(--secondary);
      color: var(--light);
      padding: 3rem 0;
      margin-top: 3rem;
    }
    
    .footer-container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 2rem;
    }
    
    .footer-column h3 {
      font-size: 1.2rem;
      margin-bottom: 1rem;
      color: var(--primary);
    }
    
    .footer-column ul {
      list-style: none;
    }
    
    .footer-column ul li {
      margin-bottom: 0.5rem;
    }
    
    .footer-column ul li a {
      color: var(--light);
      text-decoration: none;
      transition: color 0.3s;
    }
    
    .footer-column ul li a:hover {
      color: var(--primary);
    }
    
    .social-links {
      display: flex;
      gap: 1rem;
    }
    
    .social-links a {
      color: var(--light);
      font-size: 1.5rem;
    }
    
    .copyright {
      text-align: center;
      margin-top: 2rem;
      padding-top: 1rem;
      border-top: 1px solid #444;
    }
    
    /* Responsive Design */
    @media (max-width: 768px) {
      .header-container {
        flex-direction: column;
      }
      
      nav ul {
        margin-top: 1rem;
      }
      
      .hero h1 {
        font-size: 2rem;
      }
      
      .hero p {
        font-size: 1rem;
      }
      
      .jersey-grid {
        grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      }
      
      .modal-content, .auth-content {
        margin: 1rem;
        padding: 1rem;
      }
      
      .form-row {
        flex-direction: column;
        gap: 0;
      }
    }
  </style>
</head>

<body>
  <!-- Auth Modals -->
  <div class="auth-modal" id="authModal">
    <div class="auth-content">
      <span class="close-auth" onclick="hideAuthModal()">&times;</span>
      
      <div class="auth-tabs">
        <div class="auth-tab active" onclick="switchAuthTab('login')">Login</div>
        <div class="auth-tab" onclick="switchAuthTab('signup')">Sign Up</div>
      </div>
      
      <form id="loginForm" class="auth-form active" onsubmit="handleLogin(event)">
        <div class="form-group">
          <label for="loginEmail">Email</label>
          <input type="email" id="loginEmail" required>
        </div>
        <div class="form-group">
          <label for="loginPassword">Password</label>
          <input type="password" id="loginPassword" required>
        </div>
        <button type="submit" class="auth-btn">Login</button>
      </form>
      
      <form id="signupForm" class="auth-form" onsubmit="handleSignup(event)">
        <div class="form-group">
          <label for="signupName">Full Name</label>
          <input type="text" id="signupName" required>
        </div>
        <div class="form-group">
          <label for="signupEmail">Email</label>
          <input type="email" id="signupEmail" required>
        </div>
        <div class="form-group">
          <label for="signupPassword">Password</label>
          <input type="password" id="signupPassword" required>
        </div>
        <div class="form-group">
          <label for="signupPhone">Phone Number</label>
          <input type="tel" id="signupPhone">
        </div>
        <button type="submit" class="auth-btn">Sign Up</button>
      </form>
    </div>
  </div>

  <!-- Header -->
  <header>
    <div class="header-container">
      <a href="#" class="logo">
        <img src="https://via.placeholder.com/40" alt="Zenyx Jerseys Logo">
        ZENYX<span>JERSEYS</span>
      </a>
      <nav>
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#jerseys">Jerseys</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#contact">Contact</a></li>
          <li id="authLinkContainer">
            <a class="auth-link" onclick="showAuthModal()">Login/Signup</a>
          </li>
          <li>
            <a href="#" class="cart-icon" onclick="showCart()">
              🛒
              <span class="cart-count">0</span>
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero" id="home">
    <div class="hero-content">
      <h1>Premium Football Jerseys</h1>
      <p>High-quality at affordable prices. Shop the latest jerseys from top clubs and national teams.</p>
      <a href="#jerseys" class="btn">Shop Now</a>
    </div>
  </section>

  <!-- Main Content -->
  <main class="container">
    <!-- Search Bar -->
    <div class="search-bar">
      <input type="text" id="searchInput" placeholder="Search for a player or team..." oninput="searchJerseys()">
    </div>

    <!-- Jersey Grid -->
    <h2 class="section-title" id="jerseys">Our Collection</h2>
    <div class="jersey-grid" id="jersey-grid"></div>

    <!-- About Section -->
    <section id="about">
      <h2 class="section-title">About Us</h2>
      <p style="text-align: center; max-width: 800px; margin: 0 auto 2rem;">
        Zenyx Jerseys is your premier destination for high-quality football jerseys. We offer premium designs at 
        competitive prices, with a focus on customer satisfaction. Our collection includes jerseys from top clubs 
        and national teams around the world, as well as retro classics for the true football enthusiasts.
      </p>
    </section>
  </main>

  <!-- Cart Modal -->
  <div class="modal" id="cartModal">
    <div class="modal-content">
      <span class="close-modal" onclick="hideCart()">&times;</span>
      <h2>Your Cart</h2>
      <div class="cart-items" id="cart-items"></div>
      <div class="cart-total" id="cart-total">Total: ₹0</div>
      
      <div id="cartCheckoutSection">
        <button class="checkout-btn" onclick="showCheckoutForm()">Proceed to Checkout</button>
      </div>
    </div>
  </div>

  <!-- Checkout Modal -->
  <div class="modal" id="checkoutModal">
    <div class="modal-content">
      <span class="close-modal" onclick="hideCheckout()">&times;</span>
      <h2>Complete Your Order</h2>
      
      <div class="checkout-form">
        <h3>Shipping Information</h3>
        <div class="form-row">
          <div class="form-group">
            <label for="fullName">Full Name</label>
            <input type="text" id="fullName" required>
          </div>
          <div class="form-group">
            <label for="phoneNumber">Phone Number</label>
            <input type="tel" id="phoneNumber" required>
          </div>
        </div>
        
        <div class="form-group">
          <label for="address">Full Address</label>
          <textarea id="address" rows="3" required></textarea>
        </div>
        
        <div class="form-row">
          <div class="form-group">
            <label for="city">City</label>
            <input type="text" id="city" required>
          </div>
          <div class="form-group">
            <label for="state">State</label>
            <input type="text" id="state" required>
          </div>
          <div class="form-group">
            <label for="pincode">Pincode</label>
            <input type="text" id="pincode" required>
          </div>
        </div>
        
        <div class="payment-section">
          <h3>Payment Method</h3>
          <p>Please complete your payment using one of the following methods:</p>
          
          <div class="payment-methods">
            <div class="payment-method">
              <h4>Google Pay</h4>
              <div class="upi-id">
                UPI ID: 9717238838@ybl
              </div>
              <div class="qr-code">
                <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=upi://pay?pa=9717238838@ybl&pn=Zenyx%20Jerseys&mc=0000&mode=02&purpose=00" alt="Google Pay QR Code">
              </div>
            </div>
            
            <div class="payment-method">
              <h4>PhonePe/UPI</h4>
              <div class="upi-id">
                UPI ID: 7330850088@ybl
              </div>
              <div class="qr-code">
                <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=upi://pay?pa=7330850088@ybl&pn=Zenyx%20Jerseys&mc=0000&mode=02&purpose=00" alt="UPI QR Code">
              </div>
            </div>
          </div>
          
          <div style="margin-top: 2rem;">
            <h4>Payment Instructions</h4>
            <ol style="text-align: left; margin: 1rem 0; padding-left: 1.5rem;">
              <li>Scan the QR code or send payment to one of the UPI IDs above</li>
              <li>After payment, take a screenshot of the payment confirmation</li>
              <li>Upload the screenshot below</li>
              <li>Complete your order details</li>
            </ol>
            
            <div class="form-group">
              <label for="paymentScreenshot">Upload Payment Screenshot</label>
              <input type="file" id="paymentScreenshot" accept="image/*">
            </div>
          </div>
        </div>
        
        <button class="checkout-btn" onclick="completeOrder()">Complete Order</button>
      </div>
    </div>
  </div>

  <!-- Order Confirmation Modal -->
  <div class="modal" id="orderConfirmationModal">
    <div class="modal-content">
      <div class="order-confirmation">
        <h2>🎉 Order Placed Successfully!</h2>
        <h4> send screenshot of this page and the payment of the order to 9717238838 </h4> 
        <p>Thank you for your purchase. Your order has been received.</p>
        
        <div class="order-details">
          <h3>Order Summary</h3>
          <div id="orderSummary"></div>
        </div>
        
        <p>We'll send you a confirmation email shortly with your order details.</p>
        <p>For any questions, please contact us at <strong>businessgoattier@gmail.com</strong></p>
        
        <button class="btn" onclick="hideOrderConfirmation()" style="margin-top: 1rem;">Continue Shopping</button>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer>
    <div class="footer-container">
      <div class="footer-column">
        <h3>Shop</h3>
        <ul>
          <li><a href="#">All Jerseys</a></li>
          <li><a href="#">New Arrivals</a></li>
          <li><a href="#">Retro Collection</a></li>
          <li><a href="#">Special Editions</a></li>
        </ul>
      </div>
      <div class="footer-column">
        <h3>Help</h3>
        <ul>
          <li><a href="#">FAQs</a></li>
          <li><a href="#">Shipping</a></li>
          <li><a href="#">Returns</a></li>
          <li><a href="#">Size Guide</a></li>
        </ul>
      </div>
      <div class="footer-column">
        <h3>About</h3>
        <ul>
          <li><a href="#">Our Story</a></li>
          <li><a href="#">Quality</a></li>
          <li><a href="#">Privacy Policy</a></li>
          <li><a href="#">Terms of Service</a></li>
        </ul>
      </div>
      <div class="footer-column" id="contact">
        <h3>Contact</h3>
        <ul>
          <li>Email: businessgoattier@gmail.com</li>
          <li>Phone: +91 9717238838</li>
          <li>
            <div class="social-links">
              <a href="#"><span>FB</span></a>
              <a href="#"><span>IG</span></a>
              <a href="#"><span>TW</span></a>
            </div>
          </li>
        </ul>
      </div>
    </div>
    <div class="copyright">
      <p>&copy; 2023 Zenyx Jerseys. All rights reserved.</p>
    </div>
  </footer>

  <script>
    // Jersey Data with corrected image URLs
    const jerseys = [
      { name: "Lionel Messi Inter Miami 2025-26 Home Jersey", team: "Inter Miami", price: 980, img: "https://cyberriedstore.com/wp-content/uploads/2025/03/miami-2024-25-messi-home-jersey-product-cyberried-png.avif" },
      { name: "RCB Virat Kohli 2025 Official Home Jersey | IPL Jersey", team: "RCB", price: 950, img: "https://cyberriedstore.com/wp-content/uploads/2025/04/royal-challengers-Banglore9rcb-virat-kohli-jersey-product-pre-png.avif" },
      { name: "India ODI Cricket Premium Jersey", team: "India", price: 890, img: "https://cyberriedstore.com/wp-content/uploads/2025/03/India-odi-cricket-premium-quality-jersey-cyberried-store-png.avif" },
      { name: "Neymar Santos 2012-13 Home Jersey | Retro Collection", team: "SANTOS FC 2012-2013", price: 890, img: "https://cyberriedstore.com/wp-content/uploads/2024/12/Neymar-2013-14-santos-away-jersey-product-cyberried-store-png.avif" },
      { name: "Real Madrid 2002-03 Zidane Away Jersey", team: "Real Madrid 2002-2003", price: 899, img: "https://cyberriedstore.com/wp-content/uploads/2024/12/Real-madrid-2002-03-zidane-away-jersey-product-cyberried-store-png.avif" },
      { name: "Liverpool M.Salah 2024-25 Home Jersey", team: "Liverpool", price: 980, img: "https://cyberriedstore.com/wp-content/uploads/2024/12/Liverpool-2024-25-salah-home-jersey-product-png.avif" },
      { name: "C.Ronaldo Real Madrid 2010-11 Home Jersey", team: "Real Madrid", price: 970, img: "https://cyberriedstore.com/wp-content/uploads/2024/11/Real-madrid-2010-11-Cristiano-ronaldo-home-jersey-product-png.avif" },
      { name: "Real Madrid 2024-25 Bellingham Away Jersey", team: "Real Madrid", price: 960, img: "https://cyberriedstore.com/wp-content/uploads/2024/11/Real-madrid-2024-25-Bellingham-away-jersey-product-png.avif" },
      { name: "Al Nassr 2024-25 C.Ronaldo Third Jersey", team: "Al Nassr", price: 890, img: "https://cyberriedstore.com/wp-content/uploads/2024/10/Al-nassr-2024-25-critiano-ronaldo-third-jersey-product-png.avif" },
      { name: "Juventus 2024-25 Gonzalez Third Jersey", team: "Juventus", price: 899, img: "https://cyberriedstore.com/wp-content/uploads/2024/10/Juventus-2024-25-Gonzalez-third-jersey-product.png" },
      { name: "Fc Bayern Munich 2024-25 Third Jersey", team: "Fc Bayern Munich", price: 980, img: "https://cyberriedstore.com/wp-content/uploads/2024/10/Bayern-Munich-2024-25-third-jersey-product.png" },
      { name: "Manchester United Black Shorts", team: "MAN UTD", price: 470, img: "https://cyberriedstore.com/wp-content/uploads/2024/10/manchester-united-black-shorts-cyberried-store.png" },
      { name: "Fc Barcelona Yamal 2024-25 Third Jersey", team: "Fc Barcelona", price: 899, img: "https://cyberriedstore.com/wp-content/uploads/2024/10/Barcelona-2024-25-yamal-third-jersey-product-1.png" },
      { name: "Real Madrid White Shorts", team: "Real Madrid", price: 480, img: "https://cyberriedstore.com/wp-content/uploads/2024/10/real-madrid-white-shorts-cyberried-store.png" },
      { name: "Manchester United White Shorts", team: "MAN UTD", price: 470, img: "https://cyberriedstore.com/wp-content/uploads/2024/10/manchester-united-white-shorts-cyberried-store.png" },
      { name: "Fc Barcelona Blue Shorts", team: "Fc Barcelona", price: 460, img: "https://cyberriedstore.com/wp-content/uploads/2024/10/Barcelona-blue-shorts-cyberried-store.png" },
      { name: "Manchester United 2024-25 Special Edition Jersey", team: "Man Utd", price: 890, img: "https://cyberriedstore.com/wp-content/uploads/2024/09/Manchester-united-2024-25-special-jersey-product.png" },
      { name: "Neymar Santos 2012-13 Away Jersey | Retro Collection", team: "Santos Fc", price: 899, img: "https://cyberriedstore.com/wp-content/uploads/2024/09/Neymar-santos-away-jersey-product-front.png" },
      { name: "Manchester City 2024-25 Special Edition Jersey", team: "Man City", price: 980, img: "https://cyberriedstore.com/wp-content/uploads/2024/08/manchester-city-2024-25-special-edition-jersey-product.png" }
    ];

    // Initialize cart and user
    let cart = JSON.parse(localStorage.getItem('cart')) || [];
    let currentUser = JSON.parse(localStorage.getItem('currentUser')) || null;

    // Display jerseys
    function displayJerseys(filter = '') {
      const jerseyGrid = document.getElementById('jersey-grid');
      jerseyGrid.innerHTML = '';
      
      const filteredJerseys = jerseys.filter(j => 
        j.name.toLowerCase().includes(filter.toLowerCase()) || 
        j.team.toLowerCase().includes(filter.toLowerCase())
      );
      
      if (filteredJerseys.length === 0) {
        jerseyGrid.innerHTML = '<p style="grid-column:1/-1; text-align:center;">No jerseys found matching your search.</p>';
        return;
      }
      
      filteredJerseys.forEach(jersey => {
        const jerseyCard = document.createElement('div');
        jerseyCard.className = 'jersey-card';
        jerseyCard.innerHTML = `
          <img src="${jersey.img}" alt="${jersey.name}" class="jersey-img">
          <div class="jersey-info">
            <h3 class="jersey-title">${jersey.name}</h3>
            <p class="jersey-team">${jersey.team}</p>
            <p class="jersey-price">₹${jersey.price}</p>
            <select class="size-select" id="size-${jersey.name.replace(/ /g, '-')}">
              <option value="S">S</option>
              <option value="M">M</option>
              <option value="L">L</option>
              <option value="XL">XL</option>
              <option value="XXL">XXL</option>
            </select>
            <button class="add-to-cart" onclick="addToCart('${jersey.name.replace(/'/g, "\\'")}')">Add to Cart</button>
          </div>
        `;
        jerseyGrid.appendChild(jerseyCard);
      });
    }

    // Add to cart function - fixed version
    function addToCart(jerseyName) {
      if (!currentUser) {
        alert('Please login to add items to cart');
        showAuthModal();
        return;
      }
      
      // Find the jersey in our data
      const jersey = jerseys.find(j => j.name === jerseyName);
      if (!jersey) return;
      
      // Get the selected size
      const sizeSelect = document.getElementById(`size-${jerseyName.replace(/ /g, '-')}`);
      const size = sizeSelect ? sizeSelect.value : 'M';
      
      // Check if item already exists in cart
      const existingItemIndex = cart.findIndex(
        item => item.name === jerseyName && item.size === size
      );
      
      if (existingItemIndex >= 0) {
        // Item already in cart - increase quantity
        cart[existingItemIndex].quantity = (cart[existingItemIndex].quantity || 1) + 1;
        showToast(`${jerseyName} (${size}) quantity updated in cart!`);
      } else {
        // Add new item to cart
        cart.push({ 
          ...jersey, 
          size,
          quantity: 1
        });
        showToast(`${jerseyName} (${size}) added to cart!`);
      }
      
      updateCart();
    }

    // Remove from cart
    function removeFromCart(index) {
      cart.splice(index, 1);
      updateCart();
      showToast('Item removed from cart');
    }

    // Update cart display
    function updateCart() {
      localStorage.setItem('cart', JSON.stringify(cart));
      
      // Update cart count in header
      const totalItems = cart.reduce((sum, item) => sum + (item.quantity || 1), 0);
      document.querySelector('.cart-count').textContent = totalItems;
      
      // Update cart modal if open
      const cartItems = document.getElementById('cart-items');
      const cartTotal = document.getElementById('cart-total');
      
      if (cartItems) {
        cartItems.innerHTML = '';
        
        if (cart.length === 0) {
          cartItems.innerHTML = '<p style="text-align:center;">Your cart is empty</p>';
          cartTotal.textContent = 'Total: ₹0';
          return;
        }
        
        let total = 0;
        
        cart.forEach((item, index) => {
          const itemTotal = item.price * (item.quantity || 1);
          total += itemTotal;
          const cartItem = document.createElement('div');
          cartItem.className = 'cart-item';
          cartItem.innerHTML = `
            <img src="${item.img}" alt="${item.name}" class="cart-item-img">
            <div class="cart-item-details">
              <div class="cart-item-title">${item.name}</div>
              <div>Size: ${item.size}</div>
              <div>Quantity: ${item.quantity || 1}</div>
              <div class="cart-item-price">₹${itemTotal}</div>
            </div>
            <button class="remove-item" onclick="removeFromCart(${index})">&times;</button>
          `;
          cartItems.appendChild(cartItem);
        });
        
        cartTotal.textContent = `Total: ₹${total}`;
      }
    }

    // Show toast notification
    function showToast(message) {
      const toast = document.createElement('div');
      toast.className = 'toast';
      toast.textContent = message;
      document.body.appendChild(toast);
      
      setTimeout(() => {
        toast.remove();
      }, 3000);
    }

    // Show/hide cart modal
    function showCart() {
      if (!currentUser) {
        alert('Please login to view your cart');
        showAuthModal();
        return;
      }
      
      document.getElementById('cartModal').style.display = 'block';
      updateCart();
    }

    function hideCart() {
      document.getElementById('cartModal').style.display = 'none';
    }

    // Show checkout form
    function showCheckoutForm() {
      if (cart.length === 0) {
        alert('Your cart is empty!');
        return;
      }
      
      hideCart();
      document.getElementById('checkoutModal').style.display = 'block';
    }

    function hideCheckout() {
      document.getElementById('checkoutModal').style.display = 'none';
    }

    // Complete order
    function completeOrder() {
      const fullName = document.getElementById('fullName').value;
      const phoneNumber = document.getElementById('phoneNumber').value;
      const address = document.getElementById('address').value;
      const city = document.getElementById('city').value;
      const state = document.getElementById('state').value;
      const pincode = document.getElementById('pincode').value;
      const paymentScreenshot = document.getElementById('paymentScreenshot').files[0];
      
      // Validate inputs
      if (!fullName || !phoneNumber || !address || !city || !state || !pincode) {
        alert('Please fill all the required fields');
        return;
      }
      
      if (!paymentScreenshot) {
        alert('Please upload your payment screenshot');
        return;
      }
      
      // Create order object
      const order = {
        user: currentUser,
        shippingInfo: {
          fullName,
          phoneNumber,
          address,
          city,
          state,
          pincode
        },
        items: cart,
        total: cart.reduce((sum, item) => sum + (item.price * (item.quantity || 1)), 0),
        date: new Date().toISOString(),
        status: 'Pending'
      };
      
      // Send order confirmation email
      sendOrderConfirmationEmail(order);
      
      // Show confirmation
      showOrderConfirmation(order);
      
      // Clear cart
      cart = [];
      localStorage.setItem('cart', JSON.stringify(cart));
      updateCart();
      
      // Hide checkout modal
      hideCheckout();
    }

    // Send order confirmation email
    function sendOrderConfirmationEmail(order) {
      // In a real implementation, you would use a server-side script or email service
      // This is a simulation that logs the email that would be sent
      
      let emailBody = `
        New Order Received!
        
        Customer: ${order.user.name || order.user.email}
        Order Date: ${new Date(order.date).toLocaleString()}
        Order Total: ₹${order.total}
        
        Shipping Information:
        ${order.shippingInfo.fullName}
        ${order.shippingInfo.address}
        ${order.shippingInfo.city}, ${order.shippingInfo.state} - ${order.shippingInfo.pincode}
        Phone: ${order.shippingInfo.phoneNumber}
        
        Order Items:
      `;
      
      order.items.forEach(item => {
        emailBody += `\n- ${item.name} (Size: ${item.size}, Qty: ${item.quantity || 1}) - ₹${item.price * (item.quantity || 1)}`;
      });
      
      console.log('Email sent to: businessgoattier@gmail.com');
      console.log('Email content:', emailBody);
      
      // In a real implementation, you would use something like:
      /*
      fetch('https://your-email-service.com/send', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
        },
        body: JSON.stringify({
          to: 'businessgoattier@gmail.com',
          subject: `New Order #${Date.now()}`,
          text: emailBody
        }),
      });
      */
    }

    // Show order confirmation
    function showOrderConfirmation(order) {
      const orderSummary = document.getElementById('orderSummary');
      let summaryHTML = `
        <p><strong>Order Date:</strong> ${new Date(order.date).toLocaleString()}</p>
        <p><strong>Shipping To:</strong> ${order.shippingInfo.fullName}, ${order.shippingInfo.address}, ${order.shippingInfo.city}, ${order.shippingInfo.state} - ${order.shippingInfo.pincode}</p>
        <p><strong>Contact:</strong> ${order.shippingInfo.phoneNumber}</p>
        <hr style="margin: 1rem 0; border-color: #eee;">
        <h4>Order Items:</h4>
        <ul style="margin: 0.5rem 0; padding-left: 1.5rem;">
      `;
      
      order.items.forEach(item => {
        summaryHTML += `<li>${item.name} (Size: ${item.size}, Qty: ${item.quantity || 1}) - ₹${item.price * (item.quantity || 1)}</li>`;
      });
      
      summaryHTML += `
        </ul>
        <hr style="margin: 1rem 0; border-color: #eee;">
        <p><strong>Total Amount:</strong> ₹${order.total}</p>
        <p><strong>Payment Method:</strong> UPI Payment</p>
        <p><strong>Status:</strong> ${order.status}</p>
      `;
      
      orderSummary.innerHTML = summaryHTML;
      document.getElementById('orderConfirmationModal').style.display = 'block';
    }

    function hideOrderConfirmation() {
      document.getElementById('orderConfirmationModal').style.display = 'none';
    }

    // Search jerseys
    function searchJerseys() {
      const query = document.getElementById('searchInput').value;
      displayJerseys(query);
    }

    // Auth Modal Functions
    function showAuthModal() {
      document.getElementById('authModal').style.display = 'flex';
    }

    function hideAuthModal() {
      document.getElementById('authModal').style.display = 'none';
    }

    function switchAuthTab(tab) {
      document.querySelectorAll('.auth-tab').forEach(t => t.classList.remove('active'));
      document.querySelectorAll('.auth-form').forEach(f => f.classList.remove('active'));
      
      document.querySelector(`.auth-tab[onclick="switchAuthTab('${tab}')"]`).classList.add('active');
      document.getElementById(`${tab}Form`).classList.add('active');
    }

    // Handle Login
    function handleLogin(event) {
      event.preventDefault();
      const email = document.getElementById('loginEmail').value;
      const password = document.getElementById('loginPassword').value;
      
      // In a real app, you would validate credentials against a database
      currentUser = {
        email,
        name: email.split('@')[0] // Simple way to get a name from email
      };
      
      localStorage.setItem('currentUser', JSON.stringify(currentUser));
      updateUserUI();
      hideAuthModal();
      
      alert('Login successful!');
    }

    // Handle Signup
    function handleSignup(event) {
      event.preventDefault();
      const name = document.getElementById('signupName').value;
      const email = document.getElementById('signupEmail').value;
      const password = document.getElementById('signupPassword').value;
      const phone = document.getElementById('signupPhone').value;
      
      currentUser = {
        name,
        email,
        phone
      };
      
      localStorage.setItem('currentUser', JSON.stringify(currentUser));
      updateUserUI();
      hideAuthModal();
      
      alert('Account created successfully!');
    }

    // Update UI based on auth state
    function updateUserUI() {
      const authLinkContainer = document.getElementById('authLinkContainer');
      
      if (currentUser) {
        authLinkContainer.innerHTML = `
          <div class="user-profile">
            <div class="user-avatar">${currentUser.name.charAt(0).toUpperCase()}</div>
            <span>${currentUser.name}</span>
          </div>
        `;
      } else {
        authLinkContainer.innerHTML = `
          <a class="auth-link" onclick="showAuthModal()">Login/Signup</a>
        `;
      }
    }

    // Initialize the page
    document.addEventListener('DOMContentLoaded', () => {
      displayJerseys();
      updateCart();
      updateUserUI();
      
      // Close modals when clicking outside
      window.onclick = function(event) {
        if (event.target.classList.contains('modal')) {
          document.querySelectorAll('.modal').forEach(modal => {
            modal.style.display = 'none';
          });
        }
      }
    });
  </script>
</body>

</html>
