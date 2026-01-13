<script>
  const articles = [
    {
      title: "The Rise of Emerging Manager Programs in Institutional Portfolios",
      author: "Firm & Co.",
      image: "https://images.unsplash.com/photo-1460925895917-afdab827c52f?q=80&w=600&auto=format&fit=crop"
    },
    {
      title: "Why Design Matters in Alternative Investment Management",
      author: "Firm & Co.",
      image: "https://images.unsplash.com/photo-1558655146-d09347e92766?q=80&w=600&auto=format&fit=crop"
    },
    {
      title: "Building a Multi-Strategy Platform: Our Long-Term Vision",
      author: "Firm & Co.",
      image: "https://images.unsplash.com/photo-1551836022-d5d88e9218df?q=80&w=600&auto=format&fit=crop"
    }
  ];
</script>

<section class="py-12 md:py-16 overflow-hidden">
  <div class="container mx-auto px-6 md:px-12 relative">
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
      {#each articles as article}
        <div class="group cursor-pointer">
          <div class="aspect-[16/10] overflow-hidden mb-6 bg-gray-100">
            <img 
              src={article.image} 
              alt={article.title}
              class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
            />
          </div>
          <h3 class="text-xl font-light text-gray-900 mb-3 leading-snug group-hover:text-gray-600 transition-colors">
            {article.title}
          </h3>
          <p class="text-xs text-gray-500 uppercase tracking-wide">by {article.author}</p>
        </div>
      {/each}
    </div>

    <!-- Navigation Arrow -->
    <div class="absolute top-1/2 -right-4 md:right-4 transform -translate-y-1/2 hidden md:block">
      <button class="w-12 h-12 flex items-center justify-center text-gray-400 hover:text-black transition-colors" aria-label="Next">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M9 18L15 12L9 6" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </button>
    </div>
  </div>
</section>
