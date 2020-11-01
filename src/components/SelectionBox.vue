<template>
  <div class="border border-black text-center m-4 p-4">
    Vous êtes inscrit à : {{ selection.length }}
    <span v-if="numberSelection">conférence</span>
    <span v-else>conférences</span>

  </div>
  
</template>

<script>
export default {
  name: "selection-box",
  props: ['selection'],
  computed: {
    numberSelection(){
      if(this.selection.length < 2){
        return true
      }
      return false
    }
  }
}
</script>

<style>
</style>