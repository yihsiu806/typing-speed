<template>
  <v-container>
    <v-card dark>
      <v-card-text>
        <v-row justify="end">
          <v-spacer></v-spacer>
          <v-col>
            <v-row align="start">
              <v-col>速度</v-col>
              <v-col style="font-weight: bold; font-size: 28px; color: #4CAF50;">{{ speed }}</v-col>
              <v-col>
                <div class="anchor">
                  <span class="ship" style="font-size: 10px;">字</span>
                  <span class="ship" style="font-size: 18px; top: 3px; left: 12px;">/</span>
                  <span class="ship" style="font-size: 10px; left: 24px;">分鐘</span>
                </div>
              </v-col>
            </v-row>
          </v-col>
          <v-col>
            <v-row>
              <v-col>錯誤</v-col>
              <v-col style="font-weight: bold; font-size: 18px; color: #E53935;">{{ errors }}</v-col>
              <v-col style="font-size: 12px">字/分鐘</v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      speed: 0,
      errors: 0,
    }),
  }
</script>

<style scoped>
.anchor {
  position: relative;
}
.ship {
  position: absolute;
  display: inline-block;
}
</style>