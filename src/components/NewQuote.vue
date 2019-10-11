<template>
    <v-container>
        <v-row>
            <v-form>
                <v-col>
                    <label>Quote</label>
                    <v-text-field label="Filled" filled v-model="quote"></v-text-field>
                </v-col>
                <v-col>
                    <v-btn color="primary" @click.prevent="createNew">Add Quote</v-btn>
                </v-col>
            </v-form>
        </v-row>
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