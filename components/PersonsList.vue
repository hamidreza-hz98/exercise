<template>
  <v-data-table :headers="headers" :items="items" class="elevation-1" />
</template>

<script>
export default {
  props: {
    items: {
      default: () => [],
      type: Array
    }
  },

  data() {
    return {
      headers: [
        {
          text: "First name",
          value: 'firstName',
        },
        {
          text: "last name",
          value: 'lastName',
        },
        {
          text: "Age",
          value: 'age',
        },
      ],
    }
  }

}
</script>

<style>
</style>