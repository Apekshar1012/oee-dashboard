<script>
    const currentYear = new Date().getFullYear();
  </script>
  
  <footer class="footer">
    <div class="container">
      <div class="footer-grid">
        <div class="footer-logo">
          <img src="images/oee.png" alt="OEE.ai Logo" />
          <p>AI-powered productivity tools for modern industrial operations.</p>
          <div class="social-icons">
            <a href="https://twitter.com/oeeai" target="_blank" rel="noopener"><i class="fab fa-twitter"></i></a>
            <a href="https://linkedin.com/company/oeeai" target="_blank" rel="noopener"><i class="fab fa-linkedin"></i></a>
            <a href="https://facebook.com/oeeai" target="_blank" rel="noopener"><i class="fab fa-facebook"></i></a>
          </div>
        </div>
        
        <div class="footer-links">
          <h4>Product</h4>
          <ul>
            <li><a href="/features">Features</a></li>
            <li><a href="/pricing">Pricing</a></li>
            <li><a href="/case-studies">Case Studies</a></li>
            <li><a href="/integrations">Integrations</a></li>
          </ul>
        </div>
        
        <div class="footer-links">
          <h4>Resources</h4>
          <ul>
            <li><a href="/blog">Blog</a></li>
            <li><a href="/documentation">Documentation</a></li>
            <li><a href="/webinars">Webinars</a></li>
            <li><a href="/support">Support</a></li>
          </ul>
        </div>
        
        <div class="footer-links">
          <h4>Company</h4>
          <ul>
            <li><a href="/about">About</a></li>
            <li><a href="/careers">Careers</a></li>
            <li><a href="/contact">Contact</a></li>
            <li><a href="/partners">Partners</a></li>
          </ul>
        </div>
        
        <div class="footer-newsletter">
          <h4>Stay Updated</h4>
          <p>Subscribe to our newsletter for the latest updates.</p>
          <form class="newsletter-form">
            <input type="email" placeholder="Your email address" required />
            <button type="submit">Subscribe</button>
          </form>
        </div>
      </div>
      
      <div class="footer-bottom">
        <div class="copyright">
          © {currentYear} OEE.ai. All rights reserved.
        </div>
        <div class="legal-links">
          <a href="/privacy">Privacy Policy</a>
          <a href="/terms">Terms of Service</a>
        </div>
      </div>
    </div>
  </footer>
  
  <style>
    .footer {
      background-color: #1a1a2e;
      color: #ffffff;
      padding: 5rem 5% 2rem;
    }
    
    .container {
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .footer-grid {
      display: grid;
      grid-template-columns: 1.5fr repeat(3, 1fr) 1.5fr;
      gap: 2rem;
      margin-bottom: 3rem;
    }
    
    .footer-logo img {
      height: 40px;
      margin-bottom: 1rem;
    }
    
    .footer-logo p {
      color: #b0b0c0;
      margin-bottom: 1.5rem;
      line-height: 1.6;
    }
    
    .social-icons {
      display: flex;
      gap: 1rem;
    }
    
    .social-icons a {
      color: #ffffff;
      font-size: 1.5rem;
      transition: color 0.3s;
    }
    
    .social-icons a:hover {
      color: #3498db;
    }
    
    h4 {
      font-size: 1.2rem;
      margin-bottom: 1.5rem;
      color: #ffffff;
    }
    
    .footer-links ul {
      list-style: none;
      padding: 0;
      margin: 0;
    }
    
    .footer-links li {
      margin-bottom: 0.8rem;
    }
    
    .footer-links a {
      color: #b0b0c0;
      text-decoration: none;
      transition: color 0.3s;
    }
    
    .footer-links a:hover {
      color: #3498db;
    }
    
    .footer-newsletter {
      background-color: #2a2a3c;
      padding: 2rem;
      border-radius: 8px;
    }
    .footer-newsletter h4 {
      margin-bottom: 1rem;
    }
    .footer-newsletter p {
      margin-bottom: 1.5rem;
      color: #b0b0c0;
    }
    .newsletter-form {
      display: flex;
      gap: 1rem;
    }
    .newsletter-form input {
      flex: 1;
      padding: 0.8rem;
      border-radius: 4px;
      border: none;
      outline: none;
    }
    .newsletter-form button {
      background-color: #3498db;
      color: white;
      padding: 0.8rem 2rem;
      border-radius: 4px;
      border: none;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .newsletter-form button:hover {
      background-color: #2980b9;
    }
    .footer-bottom {
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-top: 1px solid #2a2a3c;
      padding-top: 2rem;
    }   
    </style>
  