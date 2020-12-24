<template>
  <v-container>
    <Word v-for="word in words" :key="" />
  </v-container>
</template>

<script>
import Word from './Word'

export default {
  name: "ArticleBoard",

  data: () => ({
    article: '',
  }),

  mounted() {
    window.addEventListener('resize', () => {
      console.log(document.body.clientWidth)
    })
  }
};
</script>

<style scoped>
.manuscript {
  border: 1px solid #90A4AE;
  border-radius: 2px;
  height: 300px;
}
.manuscript div:first-child {
  height: 5px;
  border-bottom: 1px solid #90A4AE;
}
.manuscript div:last-child {
  height: 5px;
  border-top: 1px solid #90A4AE;
}
.grid {
  display: inline-block;
  border: 1px solid #90A4AE;
  width: 30px;
  height: 30px;
}
</style>