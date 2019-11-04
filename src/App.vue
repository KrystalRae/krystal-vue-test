<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Vue Test Project</span>
        <span class="font-weight-light">FRONT END IN VUE</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/KrystalRae/"
        target="_blank"
      >
        <span class="mr-2">Krystal Randall</span>
      </v-btn>
    </v-app-bar>

    <v-content>
      <Comments/>
    </v-content>
  </v-app>
</template>

<script>
import Comments from './components/Comments';

export default {
  name: 'App',
  components: {
    Comments
  },
  data: () => ({
    //
  }),
};
</script>
