<template lang="html">
  <div>
    <!-- <select v-model="country" >
      <option :value="country.name" v-on:click="handleClick">{{country.name}}</option>
    </select> -->
    <li v-on:click="handleClick">{{country.name}}</li>
  </div>
</template>

<script>
import { eventBus } from '../main.js'
export default {
  name: 'list-component',
  props: ['country'],
  methods: {
    handleClick(){
      eventBus.$emit('country-selected', this.country)
    }
  }
}
</script>
<style lang="css" scoped>
</style>
