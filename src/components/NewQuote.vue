<template>
    <v-container>
        <label>Quote</label>
        <v-textarea background-color="teal lighten-5" label="Filled" filled auto-grow="true" v-model="quote"></v-textarea>
        <v-btn color="primary" @click.prevent="createNew">Add Quote</v-btn>
    </v-container>
</template>

<script>

    export default {
        data: () => ({
            quote: ''
  }),
  methods: {
      createNew() {
          this.$emit('quoteAdded', this.quote)
          this.quote = ''
      }
  }
    }
</script>

<style scoped>

</style>