<script>
    import { onMount } from 'svelte';
    
    const testimonials = [
      {
        content: "OEE.ai has transformed our manufacturing plant. We've reduced downtime by 37% and increased productivity across all lines.",
        author: "Sarah Johnson",
        position: "Operations Director, Global Manufacturing Inc.",
        image: "/images/testimonial1.jpg"
      },
      {
        content: "The predictive maintenance feature alone has saved us millions in potential equipment failures. The ROI is incredible.",
        author: "Michael Chen",
        position: "CTO, Precision Technologies",
        image: "/images/testimonial2.jpg"
      },
      {
        content: "Implementation was smooth and the support team went above and beyond. Now our entire team relies on OEE.ai daily.",
        author: "Elena Rodriguez",
        position: "Plant Manager, EcoFuture Systems",
        image: "/images/testimonial3.jpg"
      }
    ];
    
    let currentIndex = 0;
    let intervalId;
    
    function nextTestimonial() {
      currentIndex = (currentIndex + 1) % testimonials.length;
    }
    
    function prevTestimonial() {
      currentIndex = (currentIndex - 1 + testimonials.length) % testimonials.length;
    }
    
    onMount(() => {
      intervalId = setInterval(nextTestimonial, 5000);
      
      return () => {
        clearInterval(intervalId);
      };
    });
  </script>
  
  <section id="testimonials" class="testimonials">
    <div class="container">
      <div class="section-header">
        <h2>What Our Clients Say</h2>
        <p>Trusted by industry leaders worldwide</p>
      </div>
      
      <div class="testimonial-slider">
        <button class="nav-btn prev" on:click|preventDefault={() => {
          clearInterval(intervalId);
          prevTestimonial();
          intervalId = setInterval(nextTestimonial, 5000);
        }}>
          <i class="fas fa-chevron-left"></i>
        </button>
        
        <div class="testimonial-content">
          {#each testimonials as testimonial, i}
            <div class="testimonial" class:active={i === currentIndex}>
              <div class="quote">"{testimonial.content}"</div>
              <div class="author-info">
                <img src={testimonial.image} alt={testimonial.author} />
                <div>
                  <div class="author-name">{testimonial.author}</div>
                  <div class="author-position">{testimonial.position}</div>
                </div>
              </div>
            </div>
          {/each}
        </div>
        
        <button class="nav-btn next" on:click|preventDefault={() => {
          clearInterval(intervalId);
          nextTestimonial();
          intervalId = setInterval(nextTestimonial, 5000);
        }}>
          <i class="fas fa-chevron-right"></i>
        </button>
      </div>
      
      <div class="dots">
        {#each testimonials as _, i}
          <button 
            class="dot" 
            class:active={i === currentIndex}
            on:click|preventDefault={() => {
              clearInterval(intervalId);
              currentIndex = i;
              intervalId = setInterval(nextTestimonial, 5000);
            }}
          ></button>
        {/each}
      </div>
    </div>
  </section>
  
  <style>
    .testimonials {
      padding: 5rem 5%;
      background-color: #ffffff;
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
    
    .testimonial-slider {
      position: relative;
      display: flex;
      align-items: center;
      max-width: 900px;
      margin: 0 auto;
    }
    
    .testimonial-content {
      flex: 1;
      position: relative;
      height: 300px;
      overflow: hidden;
    }
    
    .testimonial {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      padding: 2rem;
      background-color: #f5f7fa;
      border-radius: 8px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
      opacity: 0;
      transition: opacity 0.5s ease;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    
    .testimonial.active {
      opacity: 1;
    }
    
    .quote {
      font-size: 1.2rem;
      line-height: 1.6;
      color: #1a1a2e;
      font-style: italic;
      margin-bottom: 2rem;
    }
    
    .author-info {
      display: flex;
      align-items: center;
    }
    
    .author-info img {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      object-fit: cover;
      margin-right: 1rem;
    }
    
    .author-name {
      font-weight: 600;
      color: #1a1a2e;
    }
    
    .author-position {
      color: #4a4a6a;
      font-size: 0.9rem;
    }
    
    .nav-btn {
      background: #3498db;
      color: white;
      width: 40px;
      height: 40px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      border: none;
      cursor: pointer;
      transition: background 0.3s;
      z-index: 10;
    }
    
    .nav-btn:hover {
      background: #2980b9;
    }
    
    .dots {
      display: flex;
      justify-content: center;
      margin-top: 2rem;
      gap: 0.5rem;
    }
    
    .dot {
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background-color: #e1e1e1;
      border: none;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    
    .dot.active {
      background-color: #3498db;
    }
  </style>
  