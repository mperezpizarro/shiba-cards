<script setup>
    import Refresh from './Refresh.vue';

    defineProps({
        fetched: Boolean,
        onClick: Function,
        href: String
    })
</script>

<template>
    <div class="w-full max-w-lg aspect-[9/12] mt-6 p-4 shadow-lg rounded-xl bg-white">
        <div v-show="!fetched" class="flex items-center justify-center h-full cursor-pointer" @click="onClick">
            <h2 class="text-3xl text-center font-bold">
                REVEAL YOUR <span class="font-black bg-gradient-to-r from-orange-400 to-yellow-700 text-transparent bg-clip-text">SHIBA</span>!
            </h2>
        </div>
        <div v-show="fetched" class="flex flex-col justify-between h-full">
            <img 
                :src="href" 
                alt="Shiba picture"
                class="w-full aspect-[9/10] object-cover rounded-lg"
            />
            <Refresh />
        </div>
    </div>
</template>