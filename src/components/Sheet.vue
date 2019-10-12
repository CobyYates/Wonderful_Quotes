<template>
<v-container>
    <v-sheet class="d-flex align-center justify-center" :width="width" :height="height" :elevation="elevation" :color="color">
        <v-sheet-title class="white--text"><h2>TIP: Click on a quote to delete it!</h2></v-sheet-title>
    </v-sheet>
</v-container>
    
</template>

<script>
export default {
    data: () => ({
    //   width: "100vw",
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