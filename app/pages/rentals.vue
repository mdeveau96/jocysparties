<script setup lang="ts">
  const features = [
    { icon: '💐', title: 'Premium Quality', description: 'Hand-selected décor pieces that photograph beautifully and stand up to your big day.' },
    { icon: '🚚', title: 'Delivery & Setup', description: 'We deliver, set up, and break down everything so you can focus on enjoying your event.' },
    { icon: '✨', title: 'Custom Styling', description: 'Work with our team to build a look that perfectly matches your vision and color palette.' },
  ]

  const rentalItems = [
    { icon: '🏛️', name: 'Arches & Backdrops', description: 'Floral, geometric, and classic styles', price: '150' },
    { icon: '🕯️', name: 'Candelabras', description: 'Gold, silver, and ivory finishes', price: '25' },
    { icon: '🪑', name: 'Chiavari Chairs', description: 'Available in multiple colors', price: '8' },
    { icon: '🌸', name: 'Centerpieces', description: 'Fresh floral or faux arrangements', price: '45' },
    { icon: '🎀', name: 'Table Linens', description: 'Satin, lace, sequin, and more', price: '12' },
    { icon: '💡', name: 'Fairy Lights', description: 'Warm white string lighting', price: '35' },
    { icon: '🪞', name: 'Mirror Walls', description: 'Elegant full-length panels', price: '200' },
    { icon: '🌿', name: 'Greenery Walls', description: 'Lush boxwood and floral walls', price: '250' },
  ]

  const testimonials = [
    { name: 'Maria G.', event: 'Wedding · June 2026', text: 'Jocy made our wedding look like a fairy tale. Every piece was gorgeous and the setup crew was so professional.' },
    { name: 'Alyssa R.', event: 'Quinceañera · March 2026', text: 'I could not believe how stunning everything looked. We got so many compliments. Will definitely book again!' },
    { name: 'Carmen T.', event: 'Baby Shower · January 2026', text: 'The floral arch was even more beautiful in person. Easy to work with and very responsive.' },
    { name: 'Sofia M.', event: 'Wedding · May 2026', text: 'Stress-free experience from start to finish. They handled everything and the venue was transformed!' },
  ]
</script>

<template>
  <div class="bg-(--color-wedding-linen) text-(--color-wedding-charcoal) min-h-screen">
    <!-- Hero -->
    <section class="relative bg-white py-24 px-6 text-center">
      <div class="max-w-3xl mx-auto">
        <p class="text-rose-400 uppercase tracking-widest text-sm mb-4 font-medium">Wedding & Event Decoration Rentals</p>
        <h1 class="text-5xl font-serif font-light leading-tight mb-6">
          Make Your Special Day <br /><em>Unforgettable</em>
        </h1>
        <p class="text-lg text-gray-500 mb-10 leading-relaxed">
          Elegant décor rentals for weddings, quinceañeras, baby showers, and all life's beautiful celebrations.
        </p>
        <div class="flex gap-4 justify-center flex-wrap">
          <UButton color="neutral" size="lg">Browse Rentals</UButton>
          <UButton color="neutral" variant="outline" size="lg">View Gallery</UButton>
        </div>
      </div>
    </section>

    <!-- Features -->
    <section class="py-16 px-6 bg-(--color-wedding-linen)">
      <div class="max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8 text-center">
        <div v-for="feature in features" :key="feature.title" class="bg-white rounded-2xl p-8 shadow-sm">
          <div class="text-4xl mb-4">{{ feature.icon }}</div>
          <h3 class="font-serif text-xl mb-2">{{ feature.title }}</h3>
          <p class="text-gray-500 text-sm leading-relaxed">{{ feature.description }}</p>
        </div>
      </div>
    </section>

    <!-- Rentals -->
    <section id="rentals" class="py-20 px-6 bg-white">
      <div class="max-w-6xl mx-auto">
        <div class="text-center mb-12">
          <p class="text-rose-400 uppercase tracking-widest text-sm mb-2">What We Offer</p>
          <h2 class="text-4xl font-serif font-light">Our Rental Collection</h2>
        </div>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
          <UCard v-for="item in rentalItems" :key="item.name" class="text-center hover:shadow-md transition-shadow">
            <div class="text-5xl mb-4">{{ item.icon }}</div>
            <h4 class="font-semibold mb-1">{{ item.name }}</h4>
            <p class="text-gray-400 text-xs mb-3">{{ item.description }}</p>
            <p class="text-rose-400 font-semibold text-sm">From ${{ item.price }}</p>
          </UCard>
        </div>
      </div>
    </section>


    <!-- Testimonials -->
    <section class="py-20 px-6 bg-white">
      <div class="max-w-4xl mx-auto text-center">
        <p class="text-rose-400 uppercase tracking-widest text-sm mb-2">Kind Words</p>
        <h2 class="text-4xl font-serif font-light mb-12">Happy Couples</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <UCard v-for="review in testimonials" :key="review.name" class="text-left">
            <p class="text-gray-500 italic mb-4 leading-relaxed">"{{ review.text }}"</p>
            <div class="flex items-center gap-3">
              <div class="w-10 h-10 rounded-full bg-rose-100 flex items-center justify-center text-rose-400 font-semibold">
                {{ review.name[0] }}
              </div>
              <div>
                <p class="font-semibold text-sm">{{ review.name }}</p>
                <p class="text-xs text-gray-400">{{ review.event }}</p>
              </div>
            </div>
          </UCard>
        </div>
      </div>
    </section>
  </div>
</template>
