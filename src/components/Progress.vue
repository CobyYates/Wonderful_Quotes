<template>
<v-content>
    <h3>Quotes Added</h3>
    <v-progress-linear rounded color="teal" height="20" :value="(quoteCount / maxQuotes) * 100" striped></v-progress-linear>
    {{ quoteCount }} / {{ maxQuotes }}
</v-content>
</template>

<script>
    export default {
        props: ['quoteCount', 'maxQuotes'],
    }
</script>

<style scoped>
   
</style>