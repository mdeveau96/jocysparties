<template>
    <!-- Contact -->
    <section id="contact" class="py-20 px-6 bg-(--color-wedding-linen)">
      <div class="max-w-2xl mx-auto text-center">
        <p class="text-rose-400 uppercase tracking-widest text-sm mb-2">Let's Connect</p>
        <h2 class="text-4xl font-serif font-light mb-4">Request a Quote</h2>
        <p class="text-gray-500 mb-10">Tell us about your event and we'll put together the perfect rental package for you.</p>
        <UCard>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
            <UInput placeholder="Your Name" size="lg" />
            <UInput placeholder="Email Address" type="email" size="lg" />
            <UInput placeholder="Event Date" type="date" size="lg" />
            <UInput placeholder="Guest Count" type="number" size="lg" />
          </div>
          <UTextarea placeholder="Tell us about your event..." size="xl" :rows="5" class="mb-4 w-full" autoresize />
          <UButton class="bg-rose-400 hover:bg-rose-500 text-white" block size="lg">Send Request</UButton>
        </UCard>
      </div>
    </section>
</template>
