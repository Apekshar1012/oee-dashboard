<script>
    import { onMount } from 'svelte';
    
    const features = [
      {
        icon: 'chart-line',
        title: 'Real-time Analytics',
        description: 'Monitor your production metrics in real-time with customizable dashboards and alerts.'
      },
      {
        icon: 'robot',
        title: 'AI-powered Insights',
        description: 'Leverage machine learning to predict maintenance needs and optimize production schedules.'
      },
      {
        icon: 'tools',
        title: 'Streamlined Maintenance',
        description: 'Reduce downtime with predictive maintenance and smart resource allocation.'
      },
      {
        icon: 'file-report',
        title: 'Automated Reporting',
        description: 'Generate comprehensive reports automatically for stakeholders and regulatory compliance.'
      },
      {
        icon: 'devices',
        title: 'Multi-platform Access',
        description: 'Access your operational data from any device, anytime, anywhere.'
      },
      {
        icon: 'puzzle',
        title: 'Easy Integration',
        description: 'Seamlessly connect with your existing ERP, MES, and other industrial systems.'
      }
    ];
    
    let visible = false;
    
    onMount(() => {
      const observer = new IntersectionObserver((entries) => {
        if (entries[0].isIntersecting) {
          visible = true;
        }
      }, { threshold: 0.1 });
      
      const element = document.getElementById('features-section');
      if (element) observer.observe(element);
      
      return () => {
        if (element) observer.unobserve(element);
      };
    });
  </script>
  
  <section id="features" class="features">
    <div class="container">
      <div class="section-header">
        <h2>Powerful Features for Modern Operations</h2>
        <p>Our comprehensive suite of tools helps you maximize operational efficiency</p>
      </div>
      
      <div id="features-section" class="features-grid">
        {#each features as feature, i}
          <div class="feature-card" class:visible style="transition-delay: {i * 100}ms">
            <div class="icon">
              <i class="fas fa-{feature.icon}"></i>
            </div>
            <h3>{feature.title}</h3>
            <p>{feature.description}</p>
          </div>
        {/each}
      </div>
    </div>
  </section>
  
  <style>
    .features {
      padding: 5rem 5%;
      background-color: #ffffff;
    }
    
    .container {
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .section-header {
      text-align: center;
      margin-bottom: 3rem;
    }
    
    h2 {
      font-size: 2.5rem;
      color: #1a1a2e;
      margin-bottom: 1rem;
    }
    
    .section-header p {
      font-size: 1.1rem;
      color: #4a4a6a;
      max-width: 600px;
      margin: 0 auto;
    }
    
    .features-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }
    
    .feature-card {
      background-color: #f8f9fa;
      border-radius: 8px;
      padding: 2rem;
      transition: all 0.5s ease;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
      opacity: 0;
      transform: translateY(30px);
    }
    
    .feature-card.visible {
      opacity: 1;
      transform: translateY(0);
    }
    
    .feature-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
    }
    
    .icon {
      font-size: 2rem;
      color: #3498db;
      margin-bottom: 1.5rem;
      display: inline-block;
    }
    
    h3 {
      font-size: 1.5rem;
      margin-bottom: 1rem;
      color: #1a1a2e;
    }
    
    .feature-card p {
      color: #4a4a6a;
      line-height: 1.6;
    }
  </style>
  
  