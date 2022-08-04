<template>
  <div>
    <Form @onSubmit="addToPersons($event)" />

    <PersonsList v-for="(item, index) in items" :key="index" :items="items" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [],
      showTable: true
    }
  },
  methods: {
    addToPersons(person) {
      this.items.push(person)
    }
  }

}
</script>

<style>
</style>