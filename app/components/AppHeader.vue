<script setup lang="ts">
import type { NavigationMenuItem } from "@nuxt/ui";

const route = useRoute();

const items = computed<NavigationMenuItem[]>(() => [
  {
    label: "Rentals",
    to: '/',
    active: route.path.startsWith('/rentals')
  },
  {
    label: "Our Services",
    to: '/services',
    active: route.path.startsWith('/services')
  },
  {
    label: "About Us",
    to: '/about',
    active: route.path.startsWith('/about')
  },
  {
    label: "Contact Us",
    to: '/contact',
    active: route.path.startsWith('/contact')
  },
]);
</script>

<template>
  <UHeader :ui="{ root: 'bg-(--ui-bg-color)', container: 'max-w-none', center: 'flex-1 justify-center' }">
    <template #title>
      <NuxtLink to="/" class="flex items-center gap-2 text-rose-400 hover:text-rose-500 transition-colors">
        <img src="/JocyPartyRentals-LogoZ-removebg.png" alt="Jocy's Parties" class="h-20" />
      </NuxtLink>
    </template>
    <template #left />
    <UNavigationMenu :items="items" />
    <template #right>
      <UButton class="bg-(--color-wedding-rose) text-white hover:bg-rose-700" variant="soft" size="md" to="/contact">Get a Quote</UButton>
    </template>
  </UHeader>
</template>
