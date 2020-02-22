<template>
<div style="height:100%">
  <div id="water-level-chart">
    <div class="water-level-chart-title">计划资金累计完成情况</div>

    <div class="chart-container">
      <dv-water-level-pond :config="config1" />
    </div>
  </div>
  
  <div id="water-level-chart-2">
    <div class="water-level-chart-title">计划资金累计完成情况</div>

    <div class="chart-container">
      <dv-water-level-pond :config="config2" />
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'WaterLevelChart',
  data () {
    return {
      config1: {
        data: [45],
        shape: 'round',
        waveHeight: 25,
        waveNum: 2
      },
      config2: {
        data: [70],
        shape: 'round',
        waveHeight: 25,
        waveNum: 2,
        colors: ['red','orange']
      }
    }
  }
}
</script>

<style lang="less">
#water-level-chart {
  width: 100%;
  height: 50%;
  box-sizing: border-box;
  background-color: rgba(6, 30, 93, 0.5);
  border-top: 2px solid rgba(1, 153, 209, .5);
  display: flex;
  flex-direction: column;
  padding: 5px;

  .water-level-chart-title {
    height: 15%;
    margin: 0.3vw;
    display: flex;
    align-items: center;
    font-size: 0.8vw;
    justify-content: center;
  }


  .chart-container {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .dv-water-pond-level {
    max-width: 90%;
    width: 8vw;
    height: 8vw;
    border: 10px solid #19c3eb;
    border-radius: 50%;

    ellipse {
      stroke: transparent !important;
    }

    text {
      font-size: 40px;
    }
  }
}
#water-level-chart-2 {
  width: 100%;
  height: 50%;
  box-sizing: border-box;
  background-color: rgba(6, 30, 93, 0.5);
  border-top: 2px solid rgba(1, 153, 209, .5);
  display: flex;
  flex-direction: column;
  padding: 5px;

  .water-level-chart-title {
    height: 15%;
    margin: 0.3vw;
    display: flex;
    align-items: center;
    font-size: 0.8vw;
    justify-content: center;
  }


  .chart-container {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .dv-water-pond-level {
    max-width: 90%;
    width: 8vw;
    height: 8vw;
    border: 10px solid orangered;
    border-radius: 50%;

    ellipse {
      stroke: transparent !important;
    }

    text {
      font-size: 40px;
    }
  }
}
</style>
