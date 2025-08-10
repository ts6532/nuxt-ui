<script setup lang="ts">
interface Props {
  color?: "red" | "blue";
  label?: string;
}

const { color = "red", label = "fancyButton" } = defineProps<Props>();
</script>

<template>
  <button>{{ label }}</button>
</template>

<style scoped>
button {
  background-color: v-bind(color);
}
</style>
