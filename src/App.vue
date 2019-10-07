<template>
  <v-app>
    <v-app-bar app>
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
    </v-app-bar>

    <v-content>
      <v-btn @click="selectedComponent = 'app-quote'">Quote</v-btn>
      <v-btn @click="selectedComponent = 'app-author'">Author</v-btn>
      <v-btn @click="selectedComponent = 'app-new'">New</v-btn>
      <hr>
      <p>{{ selectedComponent }}</p>
      <component :is="selectedComponent">
        <p>Default Content</p>
      </component>
      <!-- <app-quote>
        <h2 slot="title">{{ quoteTitle }}</h2>
        <p slot="content">A wonderful Quote</p>
      </app-quote> -->
    </v-content>
  </v-app>
</template>

<script>
import Quote from './components/Quote';
import Author from './components/Author';
import New from './components/New';

export default {
  
  data: () => ({
    quoteTitle: 'The Quote',
    selectedComponent: 'app-quote'
  }),
  components: {
    'app-quote': Quote,
    appAuthor: Author,
    appNew: New
  }
};
</script>
