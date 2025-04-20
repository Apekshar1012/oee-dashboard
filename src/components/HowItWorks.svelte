<script>
    const steps = [
      {
        number: '01',
        title: 'Connect Your Systems',
        description: 'Integrate OEE.ai with your existing industrial systems using our secure connectors and APIs.'
      },
      {
        number: '02',
        title: 'Configure Dashboards',
        description: 'Setup customized dashboards tailored to your specific operational needs and KPIs.'
      },
      {
        number: '03',
        title: 'Train AI Models',
        description: 'Our system learns from your historical data to identify patterns and predict future trends.'
      },
      {
        number: '04',
        title: 'Implement Solutions',
        description: 'Deploy AI-recommended strategies to optimize processes and improve efficiency.'
      }
    ];
  </script>
  
  <section id="how-it-works" class="how-it-works">
    <div class="container">
      <div class="section-header">
        <h2>How OEE.ai Works</h2>
        <p>Get started in four simple steps to transform your operations</p>
      </div>
      
      <div class="steps">
        {#each steps as step, i}
          <div class="step">
            <div class="step-number">{step.number}</div>
            <div class="step-content">
              <h3>{step.title}</h3>
              <p>{step.description}</p>
            </div>
            {#if i < steps.length - 1}
              <div class="connector"></div>
            {/if}
          </div>
        {/each}
      </div>
      
      <div class="demo-cta">
        <h3>Ready to see OEE.ai in action?</h3>
        <a href="/demo" class="primary-btn">Schedule a Demo</a>
      </div>
    </div>
  </section>
  
  <style>
    .how-it-works {
      padding: 5rem 5%;
      background-color: #f5f7fa;
    }
    
    .container {
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .section-header {
      text-align: center;
      margin-bottom: 4rem;
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
    
    .steps {
      display: flex;
      flex-direction: column;
      gap: 2rem;
      max-width: 800px;
      margin: 0 auto;
    }
    
    .step {
      display: flex;
      position: relative;
    }
    
    .step-number {
      font-size: 2.5rem;
      font-weight: 700;
      color: #3498db;
      margin-right: 2rem;
      min-width: 60px;
      text-align: center;
    }
    
    .step-content {
      flex: 1;
    }
    
    .step-content h3 {
      font-size: 1.5rem;
      margin-bottom: 0.5rem;
      color: #1a1a2e;
    }
    
    .step-content p {
      color: #4a4a6a;
      line-height: 1.6;
    }
    
    .connector {
      position: absolute;
      top: 100%;
      left: 30px;
      height: 2rem;
      width: 2px;
      background-color: #3498db;
    }
    
    .demo-cta {
      margin-top: 5rem;
      text-align: center;
      padding: 3rem;
      background-color: white;
      border-radius: 8px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    }
    
    .demo-cta h3 {
      font-size: 1.8rem;
      margin-bottom: 1.5rem;
      color: #1a1a2e;
    }
    
    .primary-btn {
      background-color: #3498db;
      color: white;
      padding: 0.8rem 2rem;
      border-radius: 4px;
      text-decoration: none;
      font-weight: 600;
      transition: background-color 0.3s;
      display: inline-block;
    }
    
    .primary-btn:hover {
      background-color: #2980b9;
    }
    
    @media (max-width: 768px) {
      .step {
        flex-direction: column;
      }
      
      .step-number {
        margin-right: 0;
        margin-bottom: 1rem;
      }
      
      .connector {
        display: none;
      }
    }
  </style>
  