<script setup>
    import ShareIcon from './ShareIcon.vue';
    import { toast } from 'wc-toast'

    defineProps({
        href: String
    })

    function handleShare(href) {
        navigator.clipboard.writeText = href

        toast("Image URL copied to clipboard!", {
            icon: {
                type: 'success'
            }
        })
    }
</script>

<template>
    <button 
        class="absolute z-20 top-6 right-6 p-2 w-fit aspect-square bg-white/40 backdrop-blur rounded-full flex items-center justify-center"
        @click="handleShare(href[0])"
    >
        <ShareIcon />
    </button>
</template>