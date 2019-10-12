<template>
    <v-container>
        <v-row sm="4" class="pt-10">
            <v-col class="text-center">
                <h3>Quotes Added</h3>
                <v-progress-linear rounded color="teal" height="20" :value="(quoteCount / maxQuotes) * 100" striped></v-progress-linear>
                {{ quoteCount }} / {{ maxQuotes }}
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        props: ['quoteCount', 'maxQuotes'],
    }
</script>

<style scoped>

</style>