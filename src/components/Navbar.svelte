<script>
    let isMenuOpen = false;
    
    function toggleMenu() {
      isMenuOpen = !isMenuOpen;
    }
  </script>
  
  <nav>
    <div class="container">
      <div class="logo">
        <a href="/">
          <img src="oee-logo.svg" alt="OEE.ai Logo" />
        </a>
      </div>
      
      <button class="menu-toggle" on:click={toggleMenu}>
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </button>
      
      <ul class="nav-links" class:active={isMenuOpen}>
        <li><a href="#features">Features</a></li>
        <li><a href="#how-it-works">How It Works</a></li>
        <li><a href="#pricing">Pricing</a></li>
        <li><a href="#testimonials">Testimonials</a></li>
        <li><a href="/blog">Blog</a></li>
        <li class="cta"><a href="/demo">Request Demo</a></li>
      </ul>
    </div>
  </nav>
  
  <style>
    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background-color: white;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
      z-index: 100;
    }
    
    .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 5%;
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .logo img {
      height: 40px;
    }
    
    .nav-links {
      display: flex;
      list-style: none;
      gap: 2rem;
      margin: 0;
      padding: 0;
    }
    
    .nav-links a {
      text-decoration: none;
      color: #333;
      font-weight: 500;
      transition: color 0.3s;
    }
    
    .nav-links a:hover {
      color: #3498db;
    }
    
    .cta a {
      background-color: #3498db;
      color: white !important;
      padding: 0.5rem 1.5rem;
      border-radius: 4px;
      transition: background-color 0.3s;
    }
    
    .cta a:hover {
      background-color: #2980b9;
    }
    
    .menu-toggle {
      display: none;
      background: none;
      border: none;
      cursor: pointer;
    }
    
    .bar {
      display: block;
      width: 25px;
      height: 3px;
      margin: 5px 0;
      background-color: #333;
      transition: all 0.3s;
    }
    
    @media (max-width: 768px) {
      .menu-toggle {
        display: block;
      }
      
      .nav-links {
        position: absolute;
        top: 70px;
        left: 0;
        flex-direction: column;
        width: 100%;
        background-color: white;
        box-shadow: 0 10px 10px rgba(0, 0, 0, 0.1);
        padding: 1rem 0;
        clip-path: polygon(0 0, 100% 0, 100% 0, 0 0);
        transition: clip-path 0.4s ease-out;
      }
      
      .nav-links.active {
        clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
      }
      
      .nav-links li {
        width: 100%;
        text-align: center;
        margin: 1rem 0;
      }
    }
  </style>
  