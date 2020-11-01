<template>
  <div class="bg-purple-300 p-2">
    <a href="#" @click="changeComponent('conf-view')">Toute les conférences</a> | 
    <a href="#" @click="changeComponent('selection-list')">Ma sélection</a>
  </div>
</template>

<script>
export default {
  name: "nav-bar",
  methods: {
    changeComponent(value) {
      this.$emit('change-component', value)
    }
  }
}
</script>

<style>
</style>