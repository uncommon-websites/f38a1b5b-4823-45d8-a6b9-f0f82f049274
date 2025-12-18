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
    <a href="/" class="hover:opacity-80 transition-opacity flex items-center space-x-3">
      <svg width="28" height="36" viewBox="0 0 90 115" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path fill-rule="evenodd" clip-rule="evenodd" d="M31.8701 9.95388L15.3109 19.4791L31.8819 29.0064L48.446 19.4812L31.8701 9.95388ZM53.2588 27.7795L36.6927 37.3058L36.6911 56.3603L53.2588 46.8319V27.7795ZM58.0696 55.1313L41.5014 64.66L58.072 74.187L74.6383 64.6605L58.0696 55.1313ZM79.4486 72.9601L62.883 82.4862V101.538L79.4486 92.0122V72.9601ZM53.2614 101.539V82.4864L36.6903 72.9591V92.012L53.2614 101.539ZM27.0694 56.3613L10.5003 46.8319V27.7788L27.0711 37.3058L27.0694 56.3613ZM27.0687 67.4269L4.48643 54.4394C2.25391 53.1554 0.878662 50.7828 0.878662 48.215V19.4801C0.878662 17.7684 1.79538 16.1867 3.28356 15.3307L28.2608 0.963381C30.4933 -0.320696 33.2439 -0.321154 35.4766 0.962171L60.474 15.3299C61.963 16.1857 62.8804 17.7679 62.8804 19.4801V46.8319L86.665 60.5111C88.1535 61.3671 89.0702 62.9489 89.0702 64.6607V93.3956C89.0702 95.9635 87.6948 98.3361 85.4621 99.62L60.4776 113.988C58.9894 114.843 57.1558 114.843 55.6673 113.988L30.6773 99.6202C28.4444 98.3365 27.0687 95.9635 27.0687 93.3954V67.4269Z" fill="black"/>
      </svg>
      <span class="font-display text-xl text-gray-900 hidden sm:block">Voyance Capital</span>
    </a>

    <!-- Navigation -->
    <nav class="hidden md:flex items-center space-x-8">
      {#each ['Strategy', 'Portfolio', 'Team', 'Insights', 'Contact'] as item}
        <a href="#{item.toLowerCase()}" class="text-gray-600 hover:text-black text-sm font-medium transition-colors">
          {item}
        </a>
      {/each}
    </nav>
  </div>
</header>
