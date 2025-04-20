
<script>
	import { onMount } from 'svelte';
	import Navbar from './components/Navbar.svelte';
	import Hero from './components/Hero.svelte';
	import Features from './components/Features.svelte';
	import HowItWorks from './components/HowItWorks.svelte';
	import Testimonials from './components/Testimonials.svelte';
	import Footer from './components/Footer.svelte';
	
	let isLoading = true;
	
	onMount(() => {
	  // Simulate loading
	  setTimeout(() => {
		isLoading = false;
	  }, 800);
	});
  </script>
  
  {#if isLoading}
	<div class="loading-screen">
	  <div class="spinner"></div>
	</div>
  {:else}
	<div class="app">
	  <Navbar />
	  <main>
		<Hero />
		<Features />
		<HowItWorks />
		<Testimonials />
	  </main>
	  <Footer />
	</div>
  {/if}
  
  <style>
	.app {
	  font-family: 'Inter', sans-serif;
	  color: #333;
	}
	
	.loading-screen {
	  position: fixed;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 100%;
	  background-color: #ffffff;
	  display: flex;
	  justify-content: center;
	  align-items: center;
	}
	
	.spinner {
	  width: 40px;
	  height: 40px;
	  border: 4px solid #f3f3f3;
	  border-top: 4px solid #3498db;
	  border-radius: 50%;
	  animation: spin 1s linear infinite;
	}
	
	@keyframes spin {
	  0% { transform: rotate(0deg); }
	  100% { transform: rotate(360deg); }
	}
  </style>