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
        header: ['Name', 'Gender', 'Age'],
        data: [
          ['Susan', 'F', '5'],
          ['Alexa', 'M', '13'],
          ['Zhou', 'F', '6'],
          ['Wang', 'F', '2'],
          ['Alice', 'M', '1'],
          ['Bob', 'M', '3'],
          ['Jack', 'M', '4'],
          ['Jonathon', 'F', '2'],
          ['Mike', 'F', '5'],
          ['Andrew', 'M', '3']
        ],
        index: true,
        columnWidth: [50, 150, 100,80],
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
