<template>
  <v-container>
    <v-card>
      <v-card-text>
        <div class="manuscript">
          <div class="gutter"></div>
          <Line/>
          <div class="devider"></div>
          <Line/>
          <div class="devider"></div>
          <Line/>
          <div class="gutter"></div>
        </div>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
import Line from './Line'
import Devider from './Line'

export default {
  name: "ArticleBoard",

  components: {
    Line,
    Devider,
  },

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