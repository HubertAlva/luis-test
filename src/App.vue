<script lang="ts" setup>
import Preparacion from '@/components/Preparacion.vue'
import Ingredientes from '@/components/Ingredientes.vue'
</script>

<template>
  <main class="bg-white max-w-4xl mx-auto my-16 rounded-3xl p-8">
    <section>
      <div>
        <img alt="Simple Omelette Recipe" class="rounded-2xl" src="/image-omelette.jpeg" />

        <h1 class="md:text-4xl text-3xl font-semibold text-start md:mt-8 mt-4 font-serif">
          Simple Omelette Recipe
        </h1>

        <p class="md:mt-6 mt-4 text-gray-600">
          An easy and quick dish, perfect for any meal. This classic omelette combines beaten eggs
          cooked to perfection, optionally filled with your choice of cheese, vegetables, or meats.
        </p>
      </div>
    </section>

    <Preparacion />

    <Ingredientes />

    <hr class="border-t-gray-300 mt-8" />
  </main>
</template>
