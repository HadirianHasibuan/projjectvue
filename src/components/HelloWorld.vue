<script setup>
import { ref } from 'vue'

const message = ref('Hello, Hadirian')

const name = ref("")

const count = ref(0)
const increment = ( ) => {
  count.value++
}

const imageUrl = ref("https://tse2.mm.bing.net/th?id=OIP.pJDcltCBQe7HFbgw1SkFpAHaHa&pid=Api&P=0&h=220")

const isvisible = ref(true)

</script>

<template>
  <h1>{{ message }}</h1>

  <input v-model="name" placeholder="Masukan nama">
  <p>Halo, {{ name }}!</p>

  <button @click="increment">tambah</button>
  <p>nilai: {{ count }}</p>

  <img :src="imageUrl" alt="Garpu">

  <button @click="isvisible = !isvisible">button</button>
  <p v-if="isvisible" > teks yang berisi rahasia dokumen negara</p>
</template>

