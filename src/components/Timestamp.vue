<template>
    <span class="timestamp">{{ props.time }}</span>
</template>
<script setup>
import { defineProps } from 'vue';
const props = defineProps(['time'])
</script>
<style scoped>
</style>