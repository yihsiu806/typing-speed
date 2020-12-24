<template>
  <v-container>
    <div class="word">
      <span>{{ word }}</span>
      <input type="text" />
    </div>
  </v-container>
</template>

<script>
export default {
  name: "Word",

  props: {
    word: String,
  },

  data: () => ({}),

  mounted() {},
};
</script>

<style scoped>
.word {
  width: 30px;
  height: 30px;
  border: 1px solid #90a4ae;
}
</style>