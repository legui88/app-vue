<template>
  <button class="btn-purple">
    {{ text }}
  </button>
</template>

<script>
export default {
  props: ['text']
}
</script>

<style scoped>
.btn-purple {
  @apply bg-purple-500 text-white font-bold py-2 px-4 rounded;
}
.btn-purple:hover {
  @apply bg-purple-700;
}
</style>