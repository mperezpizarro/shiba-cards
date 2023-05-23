<script setup>
    import ZoomIcon from '../Icons/ZoomIcon.vue';

    defineProps({
        href: String
    })
</script>

<template>
    <a 
        class="absolute z-20 top-6 left-6 p-2 w-fit aspect-square bg-white/40 backdrop-blur rounded-full flex items-center justify-center"
        :href="href[0]"
        target="_blank"
    >
        <ZoomIcon />
    </a>
</template>