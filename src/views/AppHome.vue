<template>
  <div>
    <h1>Test DSFR table refresh</h1>
    <DsfrTable :headers="headers" :rows="pets" />
    <ul>
      <li v-for="pet in pets" :key="pet[0]">{{ pet[0] }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      headers: ["H1", "H2"],
      pets: [["test", "example"]],
    }
  },
  mounted() {
    this.pets = [["new entry", "stuff"]]
  },
}
</script>
