<script>
  const managers = [
    {
      name: "EMERGING MANAGER",
      firm: "Early Stage Ventures",
      image: "https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?q=80&w=800&auto=format&fit=crop", 
      alt: "Modern office workspace"
    },
    {
      name: "NEXT-GEN PARTNER",
      firm: "Growth Capital Partners",
      image: "https://images.unsplash.com/photo-1497366216548-37526070297c?q=80&w=800&auto=format&fit=crop",
      alt: "Contemporary office environment"
    },
    {
      name: "RISING INVESTOR",
      firm: "Frontier Ventures",
      image: "https://images.unsplash.com/photo-1497366811353-6870744d04b2?q=80&w=800&auto=format&fit=crop",
      alt: "Professional workspace"
    },
    {
      name: "NEW GENERATION",
      firm: "Catalyst Fund",
      image: "https://images.unsplash.com/photo-1497215728101-856f4ea42174?q=80&w=800&auto=format&fit=crop",
      alt: "Modern office setting"
    }
  ];
</script>

<section class="pt-32 pb-16 md:pt-48 md:pb-24 overflow-hidden">
  <div class="container mx-auto px-6 md:px-12 mb-16">
    <h1 class="font-display text-5xl md:text-7xl leading-[1.1] text-gray-900 max-w-4xl">
      Curated exposure to <span class="italic font-normal">next-generation</span><br />
      venture managers.
    </h1>
  </div>

  <div class="pl-6 md:pl-12 overflow-x-auto pb-8 scrollbar-hide">
    <div class="flex space-x-1 min-w-max">
      {#each managers as manager, i}
        <div class="relative group w-[300px] md:w-[400px]">
          <div class="aspect-[3/4] overflow-hidden bg-gray-100 relative">
            <img 
              src={manager.image} 
              alt={manager.alt}
              class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105"
            />
            {#if i === 0}
              <button class="absolute bottom-4 left-4 w-8 h-8 bg-white rounded-full flex items-center justify-center hover:scale-110 transition-transform" aria-label="Pause">
                <svg width="10" height="12" viewBox="0 0 10 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <rect width="3" height="12" rx="1.5" fill="black"/>
                  <rect x="7" width="3" height="12" rx="1.5" fill="black"/>
                </svg>
              </button>
              <div class="absolute bottom-0 left-0 w-full h-1 bg-gray-200">
                <div class="h-full bg-primary-600 w-1/3"></div>
              </div>
            {/if}
          </div>
          <div class="mt-4 flex items-baseline space-x-2">
            <span class="text-xs font-bold tracking-widest uppercase text-gray-900">{manager.name}</span>
            <span class="text-xs font-serif italic text-gray-500">{manager.firm}</span>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>
