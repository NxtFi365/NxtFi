<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>NxtFi - Accept Crypto. Get Fiat Instantly.</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary-blue: #2563eb;
      --primary-accent: #34d399;
      --dark-text: #111827;
      --medium-text: #4b5563;
      --light-bg: #f3f4f6;
      --white: #ffffff;
      --card-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
    }
    
    * { 
      margin: 0; 
      padding: 0; 
      box-sizing: border-box; 
    }
    
    body { 
      font-family: 'Inter', sans-serif; 
      background: var(--light-bg); 
      color: var(--dark-text); 
      line-height: 1.6; 
    }
    
    header, section, footer { 
      padding: 60px 20px; 
      max-width: 1100px; 
      margin: auto; 
    }
    
    h1, h2, h3 { 
      margin-bottom: 20px; 
      font-weight: 700; 
    }
    
    h1 { font-size: 2.8rem; }
    h2 { font-size: 2.2rem; color: var(--primary-blue); }
    h3 { font-size: 1.5rem; }
    
    p { 
      margin-bottom: 15px; 
      color: var(--medium-text);
    }
    
    .btn { 
      background: var(--primary-blue); 
      color: var(--white); 
      padding: 12px 24px; 
      border: none; 
      border-radius: 6px; 
      text-decoration: none; 
      font-weight: 600; 
      display: inline-block; 
      margin-right: 10px; 
      transition: all 0.3s ease; 
    }
    
    .btn:hover { 
      transform: translateY(-2px); 
      box-shadow: 0 5px 15px rgba(37, 99, 235, 0.2); 
      background: #1d4ed8;
    }
    
    .btn-accent {
      background: var(--primary-accent);
    }
    
    .btn-accent:hover {
      background: #10b981;
      box-shadow: 0 5px 15px rgba(52, 211, 153, 0.2);
    }
    
    .hero { 
      text-align: center; 
      background: linear-gradient(135deg, rgba(37, 99, 235, 0.1) 0%, rgba(52, 211, 153, 0.1) 100%);
      padding-top: 100px; 
      padding-bottom: 100px; 
    }
    
    .logo {
      display: flex; 
      align-items: center; 
      justify-content: center; 
      margin-bottom: 20px;
    }
    
    .logo-text {
      font-size: 2.5rem; 
      font-weight: 800;
    }
    
    .logo-blue {
      color: var(--primary-blue);
    }
    
    .logo-green {
      color: var(--primary-accent);
    }
    
    .tagline {
      font-style: italic; 
      color: var(--primary-blue);
      margin-bottom: 30px;
    }
    
    .features, .steps, .audience { 
      display: grid; 
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); 
      gap: 30px; 
    }
    
    .feature-box, .step-box, .audience-box { 
      background: var(--white); 
      padding: 25px; 
      border-radius: 10px; 
      box-shadow: var(--card-shadow);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      border-top: 3px solid var(--primary-blue);
    }
    
    .feature-box:hover, .step-box:hover, .audience-box:hover { 
      transform: translateY(-5px); 
      box-shadow: 0 10px 20px rgba(0,0,0,0.1); 
    }
    
    footer { 
      text-align: center; 
      font-size: 0.9rem; 
      color: var(--medium-text); 
      padding: 40px 20px;
    }
    
    .footer-links a { 
      margin: 0 10px; 
      color: var(--primary-blue); 
      text-decoration: none;
      font-weight: 500;
    }
    
    .footer-links a:hover {
      text-decoration: underline;
    }
    
    .contact-info { 
      display: flex; 
      justify-content: center; 
      gap: 30px; 
      margin: 30px 0; 
      flex-wrap: wrap;
    }
    
    .contact-card { 
      background: var(--white); 
      padding: 20px; 
      border-radius: 10px; 
      box-shadow: var(--card-shadow);
      text-align: center;
      min-width: 200px;
      border-top: 3px solid var(--primary-accent);
    }
    
    .form-container { 
      background: var(--white); 
      padding: 30px; 
      border-radius: 10px; 
      box-shadow: var(--card-shadow);
      max-width: 600px; 
      margin: 0 auto; 
    }
    
    .form-group { 
      margin-bottom: 20px; 
    }
    
    .form-group label { 
      display: block; 
      margin-bottom: 8px; 
      font-weight: 600; 
      color: var(--dark-text);
    }
    
    .form-group input, 
    .form-group select, 
    .form-group textarea { 
      width: 100%; 
      padding: 12px; 
      border: 1px solid #ddd; 
      border-radius: 6px; 
      font-family: 'Inter', sans-serif; 
    }
    
    .form-group textarea { 
      height: 120px; 
    }
    
    .submit-btn { 
      background: var(--primary-blue); 
      color: var(--white); 
      padding: 12px 24px; 
      border: none; 
      border-radius: 6px; 
      font-weight: 600; 
      cursor: pointer; 
      width: 100%; 
      font-size: 16px; 
      transition: background 0.3s ease;
    }
    
    .submit-btn:hover { 
      background: #1d4ed8; 
    }
    
    .success-message { 
      display: none; 
      background: var(--primary-accent); 
      color: white; 
      padding: 15px; 
      border-radius: 6px; 
      margin-top: 20px; 
      text-align: center; 
    }
    
    @media (max-width: 768px) {
      header, section, footer {
        padding: 40px 20px;
      }
      
      h1 {
        font-size: 2.2rem;
      }
      
      h2 {
        font-size: 1.8rem;
      }
      
      .contact-info {
        flex-direction: column;
        align-items: center;
        gap: 20px;
      }
    }
  </style>
</head>
<body>

  <!-- Hero Section -->
  <header class="hero">
    <div class="logo">
      <span class="logo-text logo-blue">Nxt</span>
      <span class="logo-text logo-green">Fi</span>
    </div>
    <p class="tagline">Enabling Seamless Crypto-Fiat Payments for Everyone</p>
    <h1>Empowering Global Payments</h1>
    <p>Accept Crypto. Get Fiat Instantly.</p>
    <p>Borderless commerce meets real-time settlement with NxtFi.</p>
    <a href="#waitlist" class="btn">Join the Waitlist</a>
    <a href="#contact" class="btn btn-accent">Contact Us</a>
  </header>

  <!-- Problem Section -->
  <section>
    <h2>The Payments Gap in a Web3 World</h2>
    <p>- Crypto is booming, but traditional businesses can't accept it easily.</p>
    <p>- Existing tools are complex, volatile, or non-compliant.</p>
    <p>- Merchants need real-time, local currency settlements — not speculation.</p>
  </section>

  <!-- Solution Section -->
  <section>
    <h2>Meet NxtFi</h2>
    <p>NxtFi is your bridge between crypto payments and fiat settlements. We help global merchants, freelancers, and businesses accept crypto and get paid instantly in their local currency.</p>
  </section>

  <!-- Features -->
  <section>
    <h2>Why Businesses Choose NxtFi</h2>
    <div class="features">
      <div class="feature-box">
        <h3>Instant Fiat Settlement</h3>
        <p>Convert crypto to local currency in seconds.</p>
      </div>
      <div class="feature-box">
        <h3>Multi-Wallet Support</h3>
        <p>BTC, ETH, USDT, BNB and more.</p>
      </div>
      <div class="feature-box">
        <h3>Global Currency Access</h3>
        <p>Supports AED, INR, USD — more coming soon.</p>
      </div>
      <div class="feature-box">
        <h3>Compliance Built-in</h3>
        <p>KYC, AML and regulations integrated from day one.</p>
      </div>
      <div class="feature-box">
        <h3>POS & Merchant App</h3>
        <p>Accept crypto online or in-store with ease.</p>
      </div>
      <div class="feature-box">
        <h3>Developer API</h3>
        <p>Plug NxtFi into your existing platforms.</p>
      </div>
    </div>
  </section>

  <!-- How It Works -->
  <section>
    <h2>How It Works</h2>
    <div class="steps">
      <div class="step-box">
        <h3>1. Customer Pays in Crypto</h3>
        <p>Use BTC, ETH, USDT, or BNB.</p>
      </div>
      <div class="step-box">
        <h3>2. Real-Time Conversion</h3>
        <p>We convert it to fiat instantly, minus volatility.</p>
      </div>
      <div class="step-box">
        <h3>3. You Get Paid in Fiat</h3>
        <p>Funds settle directly into your bank or wallet.</p>
      </div>
    </div>
  </section>

  <!-- Who It's For -->
  <section>
    <h2>Who It's For</h2>
    <div class="audience">
      <div class="audience-box"><h3>E-commerce Merchants</h3></div>
      <div class="audience-box"><h3>Freelancers & Creators</h3></div>
      <div class="audience-box"><h3>Consultants & Agencies</h3></div>
      <div class="audience-box"><h3>Exporters & International Sellers</h3></div>
    </div>
  </section>

  <!-- Waitlist/Enquiry Form -->
  <section id="waitlist" style="text-align:center;">
    <h2>Join Our Waitlist</h2>
    <p>Be among the first to experience seamless crypto-fiat payments.</p>
    
    <div class="form-container">
      <form id="waitlistForm">
        <div class="form-group">
          <label for="name">Merchant/Business Name</label>
          <input type="text" id="name" name="name" required>
        </div>
        
        <div class="form-group">
          <label for="email">Email Address</label>
          <input type="email" id="email" name="email" required>
        </div>
        
        <div class="form-group">
          <label for="phone">Phone Number</label>
          <input type="tel" id="phone" name="phone" required>
        </div>
        
        <div class="form-group">
          <label for="business">Business Type</label>
          <select id="business" name="business" required>
            <option value="">Select your business type</option>
            <option value="ecommerce">E-commerce</option>
            <option value="retail">Retail Store</option>
            <option value="freelancer">Freelancer/Creator</option>
            <option value="consultant">Consultant/Agency</option>
            <option value="exporter">Exporter/International Seller</option>
            <option value="other">Other</option>
          </select>
        </div>
        
        <div class="form-group">
          <label for="location">Primary Business Location</label>
          <select id="location" name="location" required>
            <option value="">Select your location</option>
            <option value="mumbai">Mumbai, India</option>
            <option value="dubai">Dubai, UAE</option>
            <option value="canada">Canada</option>
            <option value="usa">United States</option>
            <option value="europe">Europe</option>
            <option value="other">Other</option>
          </select>
        </div>
        
        <div class="form-group">
          <label for="volume">Approximate Monthly Transaction Volume (USD)</label>
          <select id="volume" name="volume" required>
            <option value="">Select your volume</option>
            <option value="1-5k">$1,000 - $5,000</option>
            <option value="5-20k">$5,001 - $20,000</option>
            <option value="20-100k">$20,001 - $100,000</option>
            <option value="100k+">$100,000+</option>
          </select>
        </div>
        
        <div class="form-group">
          <label for="message">Additional Information (Optional)</label>
          <textarea id="message" name="message"></textarea>
        </div>
        
        <button type="submit" class="submit-btn">Submit Application</button>
      </form>
      
      <div id="successMessage" class="success-message">
        Thank you for your interest! We'll contact you shortly.
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" style="text-align:center;">
    <h2>Contact Us</h2>
    <p>Have questions? Reach out to our team.</p>
    
    <div class="contact-info">
      <div class="contact-card">
        <h3>Email</h3>
        <p>hello@nxtfi.com</p>
      </div>
      <div class="contact-card">
        <h3>Support</h3>
        <p>support@nxtfi.com</p>
      </div>
      <div class="contact-card">
        <h3>Business Inquiries</h3>
        <p>partners@nxtfi.com</p>
      </div>
    </div>
    
    <p>We're available Monday-Friday, 9AM-6PM GMT</p>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 NxtFi Innovation Inc. All rights reserved.</p>
    <div class="footer-links">
      <a href="#">About</a> | 
      <a href="#">Privacy</a> | 
      <a href="#contact">Contact</a>
    </div>
  </footer>

  <script>
    document.getElementById('waitlistForm').addEventListener('submit', function(e) {
      e.preventDefault();
      
      // Here you would typically send the form data to your server
      // For demo purposes, we'll just show the success message
      
      document.getElementById('waitlistForm').style.display = 'none';
      document.getElementById('successMessage').style.display = 'block';
      
      // Scroll to show the success message
      document.getElementById('successMessage').scrollIntoView({ behavior: 'smooth' });
    });
  </script>
</body>
</html>
