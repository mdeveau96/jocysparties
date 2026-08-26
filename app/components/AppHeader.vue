<script setup lang="ts">
import type { NavigationMenuItem } from "@nuxt/ui";

const route = useRoute();

const items = computed<NavigationMenuItem[]>(() => [
  {
    label: "Rentals",
    // to: '/docs/getting-started',
    // active: route.path.startsWith('/docs/getting-started')
  },
  {
    label: "Our Services",
    // to: '/docs/components',
    // active: route.path.startsWith('/docs/components')
  },
  {
    label: "About Us",
    // to: 'https://go.nuxt.com/figma-ui',
  },
  {
    label: "Contact Us",
    // to: 'https://github.com/nuxt/ui/releases',
  },
]);
</script>

<template>
  <UHeader :ui="{ root: 'bg-(--ui-bg-color)', container: 'max-w-none', center: 'flex-1 justify-center' }">
    <template #left />

    <UNavigationMenu :items="items" />

    <template #right>
      <UColorModeButton />
    </template>
  </UHeader>
</template>
