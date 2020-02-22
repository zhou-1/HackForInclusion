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
        header: ['Title0', 'Title1', 'Title2'],
        data: [
          ['Info', 'Content', '5'],
          ['Info', 'Content', '13'],
          ['Info', 'Content', '6'],
          ['Info', 'Content', '2'],
          ['Info', 'Content', '1'],
          ['Info', 'Content', '3'],
          ['Info', 'Content', '4'],
          ['Info', 'Content', '2'],
          ['Info', 'Content', '5'],
          ['Info', 'Content', '3']
        ],
        index: true,
        columnWidth: [50, 150, 200,100],
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
