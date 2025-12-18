<script>
  const heroes = [
    {
      name: "SARAH CHEN",
      company: "Emerging Tech Fund",
      image: "https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?q=80&w=800&auto=format&fit=crop", 
      alt: "Sarah Chen portrait"
    },
    {
      name: "MARCUS RODRIGUEZ",
      company: "NextGen Ventures",
      image: "https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?q=80&w=800&auto=format&fit=crop",
      alt: "Marcus Rodriguez portrait"
    },
    {
      name: "ELENA PETROV",
      company: "Catalyst Capital",
      image: "https://images.unsplash.com/photo-1580489944761-15a19d654956?q=80&w=800&auto=format&fit=crop",
      alt: "Elena Petrov portrait"
    },
    {
      name: "JAMES OKONKWO",
      company: "Frontier Fund",
      image: "https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?q=80&w=800&auto=format&fit=crop",
      alt: "James Okonkwo portrait"
    }
  ];
</script>

<section class="pt-32 pb-16 md:pt-48 md:pb-24 overflow-hidden">
  <div class="container mx-auto px-6 md:px-12 mb-16">
    <h1 class="font-display text-5xl md:text-7xl leading-[1.1] text-gray-900 max-w-4xl">
      Backing the <span class="italic font-normal">next generation</span><br />
      of exceptional fund managers.
    </h1>
  </div>

  <div class="pl-6 md:pl-12 overflow-x-auto pb-8 scrollbar-hide">
    <div class="flex space-x-1 min-w-max">
      {#each heroes as hero, i}
        <div class="relative group w-[300px] md:w-[400px]">
          <div class="aspect-[3/4] overflow-hidden bg-gray-100 relative">
            <img 
              src={hero.image} 
              alt={hero.alt}
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
                <div class="h-full bg-primary-500 w-1/3"></div>
              </div>
            {/if}
          </div>
          <div class="mt-4 flex items-baseline space-x-2">
            <span class="text-xs font-bold tracking-widest uppercase text-gray-900">{hero.name}</span>
            <span class="text-xs font-serif italic text-gray-500">{hero.company}</span>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>
