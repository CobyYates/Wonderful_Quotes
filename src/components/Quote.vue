<template>
    <v-container>
        <v-card x-large class="quote display-1 font-weight-light pa-4">
            <v-card-title>
                &quot;<slot></slot>&quot;
            </v-card-title>
        </v-card>
    </v-container>
</template>

<script>
</script>

<style scoped>
    .quote {
        cursor: pointer;
    }
</style>