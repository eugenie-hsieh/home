<script setup lang="ts">
interface Props {
  content: string;
}
const props = defineProps<Props>();
</script>

<template>
  <div class="pill">
    {{ props.content }}
  </div>
</template>

<style scoped lang="scss">
.pill {
  background-color: var(--pill-default);
  color: var(--grey);
  width: fit-content;
  border-radius: 6px;
  padding: 4px;
  font-family: 'Courier New';
}
</style>
