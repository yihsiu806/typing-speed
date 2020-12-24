<template>
  <v-container id="keyboard">
    <v-card>
      <v-card-text>
        <v-row>
          <div class="key" v-for="(key, index) in keys.line1" :key="`keys-line1-${index}`" :data-key-code="key.keyCode">
            {{ key.keyName[0] }}
          </div>
        </v-row>
        <v-row>
          <div class="key" v-for="(key, index) in keys.line2" :key="`keys-line2-${index}`" :data-key-code="key.keyCode">
            {{ key.keyName[0] }}
          </div>
        </v-row>
        <v-row>
          <div class="key" v-for="(key, index) in keys.line3" :key="`keys-line3-${index}`" :data-key-code="key.keyCode">
            {{ key.keyName[0] }}
          </div>
        </v-row>
        <v-row>
          <div class="key" v-for="(key, index) in keys.line4" :key="`keys-line4-${index}`" :data-key-code="key.keyCode">
            {{ key.keyName[0] }}
          </div>
        </v-row>
        <v-row>
          <div class="key" v-for="(key, index) in keys.line5" :key="`keys-line5-${index}`" :data-key-code="key.keyCode">
            {{ key.keyName[0] }}
          </div>
        </v-row>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
import line1 from '../keyCharts/chart1'
import line2 from '../keyCharts/chart2'
import line3 from '../keyCharts/chart3'
import line4 from '../keyCharts/chart4'
import line5 from '../keyCharts/chart5'

export default {
  name: "Keyboard",

  data: () => ({
    keys: {
      line1,
      line2,
      line3,
      line4,
      line5
    },
  }),

  mounted() {
    const target = document.getElementById('keyboard')
    document.addEventListener("keydown", (evt) => {
      let found = target.querySelector(`[data-key-code=${evt.code}]`)
      if (found) {
        found.classList.add('press')
      }
      console.log(evt.code);
      console.log(found)
      evt.preventDefault()
      evt.stopPropagation()
    });
    document.addEventListener("keyup", (evt) => {
      let found = target.querySelector(`[data-key-code=${evt.code}]`)
      if (found) {
        found.classList.remove('press')
      }
      console.log(evt.code)
      evt.preventDefault()
      evt.stopPropagation()
    });
  },
};
</script>

<style scoped>
.key {
  display: inline-block;
  background-color: rgba(255, 255, 255, 0.5);
  border: 1px solid silver;
  width: 25px;
  height: 25px;
}
.press {
  background-color: black;
}
</style>