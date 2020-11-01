<template>
  <div class="container w-4/5 mx-auto mt-4">
    <h1 class="text-lg font-bold">Mes conférences</h1>

    <div v-if="selection.length == 0">
      <p>Vous n'avez aucune conférence de prevu</p>
    </div>
    <div v-else>
      <div
        v-for="conf in selection"
        :key="conf.name" 
        class="border border-black my-4 p-2"
      >
        <h3>{{ conf.name }}</h3>
        <span>se deroulera le {{ conf.date }}</span>
        <span> à {{ conf.heure }}</span>
        <span> en {{ conf.salle }}</span>
      </div>
    </div>

  </div>
  
</template>

<script>
export default {
  name: "selection-list",
  props: ['selection'],
}
</script>

<style>
</style>