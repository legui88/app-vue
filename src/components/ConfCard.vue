<template>
  <div 
    class="border m-2 p-2 flex justify-between"
    :class="healthStyle"
  >
    <div>
      <h1 class="text-lg font-bold">{{ confName }}</h1>
      <p> le {{ confDate }} dans l'{{ confSalle }} à {{ confHeure }} </p>

    </div>
    <base-button
      text="Sélectionner"
      @click="addToSelection"
    >
    </base-button>
  </div>
</template>

<script>
export default {
  name: "conf-card",
  props: ['conf'],
  computed: {
    confName(){
      return this.conf.name;
    },
    confSalle(){
      return this.conf.salle
    },
    confHeure(){
      return this.conf.heure
    },
    confDate(){
      return this.conf.date
    },
  },
  methods: {
    addToSelection() {
      this.$emit('add-conf', this.conf)
    }
  }
}
</script>

<style scoped>
</style>