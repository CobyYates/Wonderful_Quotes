<template>
        <v-row>
            <v-col class="d-flex flex-wrap">
                <app-quote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">{{ quote }}</app-quote>
            </v-col>
        </v-row>
</template>

<script>
    import Quote from './Quote'

    export default {
        props: ['quotes'],
        components: {
            appQuote: Quote,
        },
        methods: {
            deleteQuote(index) {
                this.$emit('quoteDeleted', index)
            }
        }
    }
</script>

<style scoped>
   
</style>