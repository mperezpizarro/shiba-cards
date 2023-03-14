<script setup>
    function refresh() {
        window.location.reload()
    }
</script>

<template>
    <button
        @click="refresh"
        class="px-4 py-2 bg-yellow-700 text-white rounded-lg w-fit mx-auto"
    >
        Show another Shiba
    </button>
</template>