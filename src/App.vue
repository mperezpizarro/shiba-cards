<script setup>
import { ref } from 'vue';

import Link from './components/Link.vue';
import Card from './components/Card.vue';
import Loading from './components/Loading.vue';

const data = ref("Placeholder") //OG Value (null)
const loading = ref(true)
const fetched = ref(false)

/*fetch("https://shibe.online/api/shibes?count=1&httpsUrls=true")
  .then(res => res.json())
  .then(value => {
    data.value = value
    loading.value = false
  })


function handleClick() {
  fetched.value = true
}*/
</script>

<template>
  <main class="w-full min-h-screen flex items-center justify-center flex-col px-4 py-2">
    <h1 class="text-3xl font-bold mt-4">Shiba Cards</h1>
    <h2 class="text-xl text-center mt-2" style="text-wrap: balance;">The shibe.online API no longer exists. This website not functional anymore.</h2>
    <Loading v-show="loading" />
    <Card v-show="!loading" :onClick="handleClick" :fetched="fetched" :href="data" />
    <section class="mt-6 mb-4 flex flex-col gap-4 text-center">
      <p>
        Shiba inu icons created by
        <Link href="https://www.flaticon.com/free-icons/shiba-inu" title="shiba inu icons">AomAm - Flaticon</Link>
      </p>
      <p>
        Web created by
        <Link href="https://github.com/mperezpizarro" title="github profile">Dráfty</Link>
      </p>
    </section>
  </main>
</template>