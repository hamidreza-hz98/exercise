<template>
  <v-form>
    <v-container>
      {{ form }}
      <v-row>
        <v-col cols="4">
          <FirstNameInput v-model="form.firstName" />
        </v-col>
        <v-col cols="4">
          <v-text-field placeholder="Last name" v-model="form.lastName" />
        </v-col>
        <v-col cols="4">
          <v-text-field :rules="[v => !!v || 'Age is required']" placeholder="Age" v-model="form.age" />
        </v-col>
        <v-col cols="12">
          <v-btn @click="handleSubmit()">
            Add person
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </v-form>
</template>

<script>
export default {
  data() {
    return {
      form: {
        firstName: "",
        lastName: "",
        age: null
      }
    };
  },
  methods: {
    clearForm() {
      this.form = {
        firstName: "",
        lastName: "",
        age: null
      };
    },
    handleSubmit() {
      this.$emit("onSubmit", this.form);
      this.clearForm();
    }
  },
}
</script>

<style>
</style>