
<script>
    import { fly, fade } from 'svelte/transition';
  </script>
  
  <section class="hero">
    <div class="container">
      <div class="hero-content">
        <div in:fly={{ y: 50, duration: 1000 }} class="text-content">
          <h1>AI-Powered Productivity for Industrial Operations</h1>
          <p>Leverage artificial intelligence to optimize your manufacturing processes, reduce downtime, and increase operational efficiency.</p>
          <div class="cta-buttons">
            <a href="/demo" class="primary-btn">Request Demo</a>
            <a href="#features" class="secondary-btn">Learn More</a>
          </div>
        </div>
        <div in:fade={{ delay: 300, duration: 1000 }} class="hero-image">
          <img src="images/dashboard.png" alt="OEE.ai Dashboard" />
        </div>
      </div>
    </div>
  </section>
  
  <style>
    .hero {
      padding: 10rem 5% 5rem;
      background: linear-gradient(135deg, #f5f7fa 0%, #e4e8ef 100%);
    }
    
    .container {
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .hero-content {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2rem;
      align-items: center;
    }
    
    h1 {
      font-size: 3rem;
      line-height: 1.2;
      margin-bottom: 1.5rem;
      color: #1a1a2e;
    }
    
    p {
      font-size: 1.2rem;
      line-height: 1.6;
      color: #4a4a6a;
      margin-bottom: 2rem;
    }
    
    .cta-buttons {
      display: flex;
      gap: 1rem;
    }
    
    .primary-btn {
      background-color: #3498db;
      color: white;
      padding: 0.8rem 2rem;
      border-radius: 4px;
      text-decoration: none;
      font-weight: 600;
      transition: background-color 0.3s;
    }
    
    .primary-btn:hover {
      background-color: #2980b9;
    }
    
    .secondary-btn {
      background-color: transparent;
      color: #3498db;
      padding: 0.8rem 2rem;
      border-radius: 4px;
      text-decoration: none;
      font-weight: 600;
      border: 2px solid #3498db;
      transition: all 0.3s;
    }
    
    .secondary-btn:hover {
      background-color: rgba(52, 152, 219, 0.1);
    }
    
    .hero-image img {
      width: 100%;
      border-radius: 8px;
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
    }
    
    @media (max-width: 768px) {
      .hero-content {
        grid-template-columns: 1fr;
      }
      
      h1 {
        font-size: 2.5rem;
      }
      
      .hero {
        padding: 8rem 5% 3rem;
      }
    }
  </style>
