<script setup>
defineProps({
    href: String,
    title: String
})
</script>

<template>
    <a :href="href" :title="title" class="text-gray-900 font-bold hover:underline">
        <slot></slot>
    </a>
</template>