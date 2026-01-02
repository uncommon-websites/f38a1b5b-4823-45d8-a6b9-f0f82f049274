<script>
  const articles = [
    {
      title: "Why Next-Gen Fund Managers Are Outperforming Traditional VCs",
      author: "Thomas Meier",
      image: "/generated/image-business-professional-working-at-desk-re-1767357585410-5.webp"
    },
    {
      title: "The New Breed of European Venture: Specialized, Agile, Thesis-Driven",
      author: "Tobias Gunzenhauser",
      image: "/generated/image-modern-european-startup-office-with-team-1767357587914-6.webp"
    },
    {
      title: "Building a Better LP for a New Generation of Managers",
      author: "Henrik Reimavuo",
      image: "/generated/image-professional-handshake-between-business--1767357590486-7.webp"
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
