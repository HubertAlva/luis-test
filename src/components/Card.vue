<script lang="ts" setup>
const props = defineProps<{
  title: string
  description: string
  image?: string
  isFeatured?: boolean
}>()
</script>

<template>
  <div
    class="mx-auto border-gray-400 rounded-lg shadow-xl group max-w-72 hover:bg-sky-200/40 transition-colors duration-500"
  >
    <div>
      <img v-if="props.image" :alt="props.title" :src="props.image" class="rounded-t-lg" />

      <img v-else alt="Placeholder" src="https://picsum.photos/300/200" />
    </div>

    <div class="p-5 space-y-4">
      <h1
        class="text-black text-3xl group-hover:text-4xl group-hover:text-primary group-hover:animate-bounce"
      >
        {{ props.title }}
      </h1>

      <p class="text-gray-600 text-sm">
        {{ props.description }}
      </p>

      <div v-if="props.isFeatured" class="bg-yellow-400 text-black rounded-3xl px-4 py-1">
        Esta tarjeta es destacada
      </div>
    </div>
  </div>
</template>
