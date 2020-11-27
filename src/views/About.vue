<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>

<script lang="ts">
import { onMounted } from "vue";
import anichart from "anichart";
interface AniBarChart {
  loadCsv: Function;
  initCanvas: Function;
  readyToDraw: Function;
}
export default {
  setup() {
    onMounted( async () => {
      console.log("222");
      const chart = new anichart.Bar();
      console.log(chart);
      // await (<AniBarChart>chart).loadCsv("./data.csv");
      // chart.initCanvas();
      // chart.readyToDraw();
    });
  }
}
</script>
