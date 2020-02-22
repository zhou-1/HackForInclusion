<template>
  <div id="data-view">
    <dv-full-screen-container>
      
      <top-header />

      <div class="main-content">

        <div class="center">
          <div class="center-left">
            <div class="element">
              <scroll-board />
            </div>
            <div class="element">
              <pointChart/>
            </div>
          </div>
          <div class="center-mid">
            <div class="element" style=" height:50%">
              <mapChart/>
            </div>
            <div class="element" style="height:50%">
              <cards />
            </div>
          </div>
          <div class="center-right-1">
            <div class="element">
              <ranking-board />
            </div>
            <div class="element">
              <water-level-chart />
            </div>
          </div>
          <div class="center-right-2">
            <div class="element">
              <curveChart/>
            </div>
            <div class="element">
              <rose-chart />
            </div>
          </div>
        </div>
        <digital-flop />
      </div>
    </dv-full-screen-container>
  </div>
</template>

<script>
import mapChart from './map'
import pointChart from './pointChart'
import topHeader from './topHeader'
import digitalFlop from './digitalFlop'
import rankingBoard from './rankingBoard'
import roseChart from './roseChart'
import waterLevelChart from './waterLevelChart'
import scrollBoard from './scrollBoard'
import cards from './cards'
import curveChart from './curveChart'

export default {
  name: 'DataView',
  components: {
    topHeader,
    digitalFlop,
    rankingBoard,
    roseChart,
    waterLevelChart,
    scrollBoard,
    cards,
    mapChart,
    pointChart,
    curveChart
  },
  data () {
    return {}
  },
  methods: {}
}
</script>

<style lang="less">
#data-view {
  width: 100%;
  height: 100%;
  background-color: #030409;
  color: #fff;

  #dv-full-screen-container {
    background-image: url('./img/bg.png');
    background-size: 100% 100%;
    box-shadow: 0 0 3px blue;
    display: flex;
    flex-direction: column;
  }

  .main-content {
    display: flex;
    width: 100%;
    height: 100%;
    flex-direction: column;
  }

  .center {
    flex: 1;
    display: flex;
    margin-top: 20px;
    width: 100%;
    justify-content: space-between;
    padding: 10px;
    height: 100%;
  }
  .left-table-area {
    height: 55%;
  }
  
  .center-left {
    flex-direction: column;
    width: 20%;
    height: 100%;
  }

  .element {
    height: 50%;
    padding: 10px;
    max-height: 50%;
  }  
  .center-mid {
    flex-direction: column;
    width: 40%;
    height: 100%;
  }
  .center-right-1 {
    flex-direction: column;
    width: 13%;
    height: 100%;
  }
  .center-right-2 {
    flex-direction: column;
    width: 28%;
    height: 100%;
  }
  .block-top-content {
    height: 55%;
    display: flex;
    flex-grow: 0;
    box-sizing: border-box;
  }
}
</style>
