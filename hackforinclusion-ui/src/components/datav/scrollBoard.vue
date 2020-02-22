<template>
  <div id="scroll-board">
    <dv-scroll-board :config="config" />
  </div>
</template>

<script>
export default {
  name: 'ScrollBoard',
  data () {
    return {
      config: {
        header: ['School', '#Homeless', '#At Rist','#Social Workers'],
        data: [
          ['Boston Latin', '10', '5','2'],
          ['Excel Middle', '2', '13','1'],
          ['Brighton High', '30', '6','7'],
          ['Fenway High', '1', '2','5'],
          ['JFK Middle', '2', '1','6'],
          ['MLK Middle', '4', '3','81'],
          ['Lincoln High', '8', '4','4'],
          ['Franklin Elem', '2', '2','8'],
          ['Washington High', '7', '5','5'],
          ['Roosevelt Elem', '2', '3','4']
        ],
        index: false,
        columnWidth: [200, 100,100,100],
        align: ['center'],
        rowNum: 7,
        headerBGC: '#1981f6',
        headerHeight: 45,
        oddRowBGC: 'rgba(0, 44, 81, 0.8)',
        evenRowBGC: 'rgba(10, 29, 50, 0.8)'
      }
    }
  }
}
</script>

<style lang="less">
#scroll-board {
  width: 100%;
  height: 100%;
  box-sizing: border-box;
  overflow: hidden;
}
</style>
