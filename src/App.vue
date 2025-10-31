<script lang="ts" setup>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import Card from '@/components/Card.vue'
import { ref } from 'vue'

const data = [
  {
    title: 'Titulo 1',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet, quod.',
  },

  {
    title: 'Titulo 2',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet, quod.',
  },

  {
    title: 'Titulo 3',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet, quod.',
    isFeatured: true,
  },

  {
    title: 'Titulo 4',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet, quod.',
  },

  {
    title: 'Titulo 5',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet, quod.',
  },
]

const hideCards = ref(false)
</script>

<template>
  <Header />

  <main v-if="!hideCards" class="pt-16 grid gap-4 md:grid-cols-2">
    <div class="mx-auto border-gray-400 rounded-lg shadow-xl max-w-72">
      <div>
        <img alt="" class="rounded-t-lg" src="https://picsum.photos/300/200" />
      </div>

      <div class="p-5 space-y-4">
        <h1 class="text-black text-3xl">Lorem ipsum dolor sit amet.</h1>

        <p class="text-gray-600 text-sm">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi cum hic mollitia nesciunt,
          nostrum nulla provident quas ut vel veritatis.
        </p>
      </div>
    </div>

    <Card
      v-for="(tarjeta, index) in data"
      :key="index"
      :description="tarjeta.description"
      :isFeatured="tarjeta.isFeatured"
      :title="tarjeta.title"
    />
  </main>

  <main v-else>Las tarjetas están ocultas.</main>

  <button
    class="px-4 py-2 rounded-full bg-black text-white cursor-pointer mt-4"
    type="button"
    @click="hideCards = !hideCards"
  >
    <template v-if="hideCards"> Mostrar tarjetas </template>

    <template v-else> Ocultar tarjetas </template>
  </button>

  <Footer />
</template>

<style scoped></style>
