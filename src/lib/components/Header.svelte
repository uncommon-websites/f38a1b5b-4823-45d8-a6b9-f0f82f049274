<script lang="ts">
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 10;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<header class="fixed top-0 left-0 w-full z-50 transition-all duration-300 {isScrolled ? 'bg-white/90 backdrop-blur-sm py-4 shadow-sm' : 'bg-transparent py-8'}">
  <div class="container mx-auto px-6 md:px-12 flex justify-between items-center">
    <!-- Logo -->
    <a href="/" class="text-black hover:opacity-80 transition-opacity">
      <span class="font-display text-xl md:text-2xl">Voyance Capital</span>
    </a>

    <!-- Navigation -->
    <nav class="hidden md:flex items-center space-x-8">
      {#each ['Team', 'Philosophy', 'Fund Managers', 'Insights', 'Resources'] as item}
        <a href="#{item.toLowerCase().replace(' ', '-')}" class="text-gray-600 hover:text-black text-sm font-medium transition-colors">
          {item}
        </a>
      {/each}
      
      <button class="text-gray-600 hover:text-black transition-colors ml-4" aria-label="Search">
        <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="11" cy="11" r="8"></circle>
          <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
        </svg>
      </button>
    </nav>
  </div>
</header>
