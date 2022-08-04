<template>
    <div>
        <v-text-field :rules="[v => !!v || 'First name is required']" placeholder="First name" :value="value"
            @input="handleInput($event)" />
    </div>
</template>

<script>
export default {
    name: 'FirstNameInput',
    props: ['value'],
    methods: {
        handleInput($event) {
            this.$emit('input', $event)
        }
    }
}
</script>

<style>
</style>