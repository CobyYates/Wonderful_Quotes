<template>
    <v-sheet class="text-center" :width="width" :height="height" :elevation="elevation" :color="color">
        <v-sheet-title>Info: Click on a quote to delete it!</v-sheet-title>
    </v-sheet>
</template>

<script>
export default {
    data: () => ({
      width: "100vw",
      height: "100",
      elevation: "4",
      color: 'error',
    }),
  }
</script>

<style scoped>
   .v-input__slider, .v-select {
  width: 100%;
}
</style>