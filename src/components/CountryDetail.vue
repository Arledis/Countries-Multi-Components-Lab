<template lang="html">
  <div v-if="country">
    <h3>{{country.name}}</h3>
    <p>Capital: {{country.capital}}</p>
    <p>Population: {{country.population}}</p>
    <p>Languages: {{country.languages[0].name}}</p>
    <p>Currency: {{country.currencies[0].name}}</p>
    <img class="lrg-flag" :src="country.flag" />
  </div>
</template>

<script>
export default {
  name: 'country-detail',
  props: ['country']
}
</script>

<style lang="css" scoped>
  .lrg-flag {
  height: 300px
}
</style>
