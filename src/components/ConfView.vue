<template>

  <div class="flex">
    <div class="w-1/5">
      <selection-box
        :selection="selection"
      >
      </selection-box>
    </div>
    

    <div class="w-4/5 mt-2">
      <conf-card 
        v-for="(conf, index) in team.conf"
        :key="index"
        :conf="conf"
        @add-conf="addconfToSelection"
        >
      </conf-card>
    </div>
    

  </div>
    
</template>

<script>
import teamData from '../data/conf.json'
import ConfCard from './ConfCard.vue'
import SelectionBox from './SelectionBox.vue'
export default {
  name: "conf-view",
  components: {
    ConfCard,
    SelectionBox
  },
  data() {
    return {
      team: teamData,
      selection: []
    }
  },
  methods: {
    addconfToSelection(conf){
      this.selection.push(conf)
      this.$emit('child-event', conf)
    }
  }
}
</script>

<style scoped>
</style>