<template>
  <v-app>
    <!-- <v-app-bar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Vuetify</span>
        <span class="font-weight-light">MATERIAL DESIGN</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">Latest Release</span>
      </v-btn>
    </v-app-bar> -->

    <v-container class="text-center" >
      <v-row align="center" justify="center">
        <v-col cols="8" sm="12">
          <app-progress :quoteCount='quotes.length' :maxQuotes='maxQuotes'></app-progress>
        </v-col>
      </v-row>
      <v-row align="center" justify="center">
        <v-col cols="12">
          <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        </v-col>
      </v-row>
      <v-row>
        <v-col class="d-flex flex-wrap">
          <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
        </v-col>
      </v-row>
      <v-row align="center">
        <v-col cols="12">
          <app-sheet></app-sheet>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
import QuoteGrid from './components/QuoteGrid';
import NewQuote from './components/NewQuote';
import Sheet from './components/Sheet'
import Progress from './components/Progress'

export default {
  
  data: () => ({
    maxQuotes: 10,
    quotes: [
      'Just a quote'
    ],
    maxQuotes: 10
  }),
  methods: {
    newQuote(quote) {
      if(this.quotes.length >= this.maxQuotes) {
        return alert('Please delete quotes first!')
      }
      this.quotes.push(quote)
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1)
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appSheet: Sheet,
    appProgress: Progress,
  }
};
</script>

<style scoped>
</style>