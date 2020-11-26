<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";
import anichart from "anichart";
export default class About extends Vue {
  async onMounted() {
    console.log("222")
    const chart = new anichart.Bar();
    await chart.loadCsv("./data.csv");
    chart.initCanvas();
    chart.readyToDraw();
  }
}
</script>
