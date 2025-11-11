<script lang="ts" setup>
const ingredients = [
  '2-3 large eggs',
  'Salt, to taste',
  'Pepper, to taste',
  '1 tablespoon of butter or oil',
  'Optional fillings: cheese, diced vegetables, cooked meats, herbs',
]
</script>

<template>
  <section class="mt-8">
    <h2 class="text-rose-800 font-bold text-3xl font-serif">Ingredients</h2>
    <ol class="list-disc marker:text-rose-800 list-inside space-y-2 mt-4">
      <li v-for="ingredient in ingredients" :key="ingredient">{{ ingredient }}</li>
    </ol>
  </section>
</template>
