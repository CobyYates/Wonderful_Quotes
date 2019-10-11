<template>
    <v-container>
        <v-row>
            <v-col cols="4">
                <app-quote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">{{ quote }}</app-quote>
            </v-col>
        </v-row>
    </v-container>
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