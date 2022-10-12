<template>
    <span class="user">
        <span class="name">{{ props.userData.name }}</span>
        <span class="handle">{{ "@" + props.userData.handle }}</span>
    </span>
</template>
<script setup>
import { defineProps } from "vue";
const props = defineProps(["userData"]);


</script>
<style scoped>

</style>