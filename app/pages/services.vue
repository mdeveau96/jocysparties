<script setup lang="ts">
const packages = [
    {
      name: 'Intimate',
      price: '499',
      featured: false,
      includes: ['1 Arch or Backdrop', '10 Centerpieces', 'Table Linens (10 tables)', 'Candelabras (10)', 'Delivery & Pickup'],
    },
    {
      name: 'Classic',
      price: '999',
      featured: true,
      includes: ['1 Arch + Greenery Wall', '20 Centerpieces', 'Table Linens (20 tables)', 'Chiavari Chairs (100)', 'Fairy Lights', 'Delivery, Setup & Pickup'],
    },
    {
      name: 'Luxe',
      price: '1,799',
      featured: false,
      includes: ['2 Arches + Mirror Wall', '30 Centerpieces', 'Premium Linens (30 tables)', 'Chiavari Chairs (200)', 'Full Lighting Package', 'Dedicated Stylist'],
    },
  ]
</script>

<template>
    <!-- Packages -->
    <section id="packages" class="py-20 px-6 bg-(--color-wedding-linen)">
      <div class="max-w-5xl mx-auto">
        <div class="text-center mb-12">
          <p class="text-rose-400 uppercase tracking-widest text-sm mb-2">Bundles</p>
          <h2 class="text-4xl font-serif font-light">Event Packages</h2>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <UCard v-for="pkg in packages" :key="pkg.name" :class="['text-center', pkg.featured ? 'ring-2 ring-rose-300' : '']">
            <p v-if="pkg.featured" class="text-rose-400 text-xs uppercase tracking-widest mb-2 font-semibold">Most Popular</p>
            <h3 class="text-2xl font-serif mb-2">{{ pkg.name }}</h3>
            <p class="text-3xl font-bold mb-4">${{ pkg.price }}<span class="text-sm font-normal text-gray-400">/event</span></p>
            <ul class="text-sm text-gray-500 space-y-2 mb-6 text-left">
              <li v-for="item in pkg.includes" :key="item" class="flex items-center gap-2">
                <span class="text-rose-300">✓</span> {{ item }}
              </li>
            </ul>
            <UButton :color="pkg.featured ? 'primary' : 'neutral'" :variant="pkg.featured ? 'solid' : 'outline'" block>
              Select Package
            </UButton>
          </UCard>
        </div>
      </div>
    </section>
</template>
