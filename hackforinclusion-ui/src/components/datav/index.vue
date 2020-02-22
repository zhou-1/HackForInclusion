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
          <div class="center-right">
            <div class="element">
              <div class="center-right-1">
                <ranking-board />
              </div>
              <div class="center-right-2">
                <curveChart/>
              </div>
            </div>
            <div class="element" style="padding:10px">
              <roseChart/>
            </div>
          </div>
        </div>
        <!--digital-flop /-->
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
    height: 70vh;
  }
  .left-table-area {
    height: 50%;
  }
  
  .center-left {
    flex-direction: column;
    width: 25%;
    height: 100%;
  }

  .element {
    height: 50%;
    padding: 10px;
    max-height: 50%;
    width:100%;
  }  
  .center-mid {
    flex-direction: column;
    width: 45%;
    height: 100%;
  }
  .center-right {
    width: 45%;
    height: 100%;
    .center-right-1{
      width: 30%;
      height: 100%;
      float: left;
      padding: 0 5px;
    }
    
    .center-right-2 {
      flex-direction: column;
      width: 70%;
      height: 100%;
      float: left;
      padding: 0 5px;
    }
  }
  
}
</style>
