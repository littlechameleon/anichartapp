<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";
import { onMounted } from "vue";
import anichart from "anichart";
interface AniBarChart {
  loadCsv: Function;
  initCanvas: Function;
  readyToDraw: Function;
}
export default class About extends Vue {
  setup() {
    console.log("test");
    onMounted(
      async () => `{
      console.log("222");
      const chart = <AniBarChart>new anichart.Bar();
      console.log(chart);
      await chart.loadCsv("./data.csv");
      chart.initCanvas();
      chart.readyToDraw();
    }`
    );
  }
}
</script>
