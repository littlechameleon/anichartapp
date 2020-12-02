<template>
  <div class="about">
  </div>
</template>

<script lang="ts">
import { onMounted } from "vue";
import * as anichart from "anichart";
export default {
  setup() {
    onMounted( async () => {
      const chart = new anichart.Bar();
      await (chart as any).loadCsv("../../data/test-meta.csv");
      (chart as any).initCanvas();
      (chart as any).readyToDraw();
      console.log(chart);

      (chart as any).play()
    });

  }
}
</script>
