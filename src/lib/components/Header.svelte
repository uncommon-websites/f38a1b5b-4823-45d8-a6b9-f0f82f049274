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
    <a href="/" class="text-gray-900 hover:text-primary-600 transition-colors">
      <span class="font-display text-2xl tracking-tight">Firm & Co.</span>
    </a>

    <!-- Navigation -->
    <nav class="hidden md:flex items-center space-x-8">
      {#each ['Strategy', 'Managers', 'Philosophy', 'Insights', 'Contact'] as item}
        <a href="#{item.toLowerCase()}" class="text-gray-600 hover:text-black text-sm font-medium transition-colors">
          {item}
        </a>
      {/each}
      
      <a href="#lp-portal" class="text-gray-600 hover:text-black transition-colors ml-4 text-sm font-medium">
        LP Portal
      </a>
    </nav>
  </div>
</header>
