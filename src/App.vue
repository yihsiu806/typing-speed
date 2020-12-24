<template>
  <v-app color="blue-grey darken-4">
    <v-main>
      <v-container>
        <v-row><ScoreBoard /></v-row>
        <v-row><ArticleBoard /></v-row>
        <v-row><Keyboard /></v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import ScoreBoard from './components/ScoreBoard';
import ArticleBoard from './components/ArticleBoard';
import Keyboard from './components/Keyboard';

export default {
  name: 'App',

  components: {
    ScoreBoard,
    ArticleBoard,
    Keyboard,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
body {
  min-width: 300px;
}
</style>