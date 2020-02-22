<template>
    <div class="curveChart">
        <div class="title">Data Title</div>
        <vue-funnel-graph :width="width" :height="height" :labels="labels"
                :values="values" :colors="colors" :sub-labels="subLabels" :direction="direction"
                :gradient-direction="gradientDirection"
                :animated="true" :display-percentage="true" style="width:100%;height:28vh"/>  
    </div>

</template>
<script>
import { VueFunnelGraph } from 'vue-funnel-graph-js';
export default {
    name: 'curveChart',
    components: {
        VueFunnelGraph
    },
    data() {
        return {
            labels: ['Impressions', 'Add To Cart', 'Buy'],
            subLabels: ['Direct', 'Social Media', 'Ads'],
            values: [
            // with the given Labels and SubLabels here's what the values represent:
            // 
            // Direct, Social, Ads  
            //    |      |     |  
            //    v      v     v
                [3000, 2500, 6500], // Segments of "Impressions" from top to bottom
                [3000, 1700, 1000], // Segments of "Add To Cart"
                [600,  200,  130]   // Segments of "Buy"
            ],
            colors: [
                ['#FFB178', '#FF3C8E'], // color set for "Impressions" segment
                ['#A0BBFF', '#EC77FF'], // color set for "Add To Cart" segment
                ['#A0F9FF', '#7795FF']  // color set for "Buy" segment
            ],
            direction: 'horizontal',
            gradientDirection: 'horizontal',
            height: 300,
            width: 800
        };
    }
}
</script>

<style>
.curveChart{
    padding: 5px;
  background-color: rgba(6, 30, 93, 0.5);
  border-top: 2px solid rgba(1, 153, 209, .5);
  height: 100%;
  width: 100%;
  flex-direction: column;
  overflow: hidden;
}
.title {
    height: 10%;
    font-weight: bold;
    text-indent: 20px;
    font-size: 20px;
    align-items: center;
  }
</style>