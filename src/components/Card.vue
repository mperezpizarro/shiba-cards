<script setup>
    import ShareButton from './Buttons/ShareButton.vue';
    import ZoomButton from './Buttons/ZoomButton.vue';

    defineProps({
        fetched: Boolean,
        onClick: Function,
        href: String
    })

    function refresh() {
        window.location.reload()
    }
</script>

<template>
    <div class="w-full max-w-lg aspect-[9/12] mt-6 p-4 shadow-lg rounded-xl bg-white relative">
        <div v-show="!fetched" class="flex items-center justify-center h-full cursor-pointer" @click="onClick">
            <h2 class="text-3xl text-center font-bold">
                REVEAL YOUR <span class="font-black bg-gradient-to-r from-orange-400 to-yellow-700 text-transparent bg-clip-text">SHIBA</span>!
            </h2>
        </div>
        <ShareButton v-show="fetched" :href="href" />
        <ZoomButton v-show="fetched" :href="href" />
        <div v-show="fetched" @click="refresh" class="flex flex-col justify-between h-full cursor-pointer">
            <img 
                :src="href" 
                alt="Shiba picture"
                class="w-full aspect-[9/11] object-cover rounded-lg"
            />
            <h4 class="font-bold text-center">Click again to reveal a new Shiba</h4>
        </div>
    </div>
</template>