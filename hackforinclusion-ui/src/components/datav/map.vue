<template>
  <div id="map">
    <dv-flyline-chart-enhanced :config="config" style="width:100%;height:100%;" class="bgimg" />
  </div>
</template>

<script>
export default {
  name: 'MapChart',
  data: ()=>({
        config:{
            points: [
                {
                name: 'Boston',
                coordinate: [0.48, 0.35],
                halo: {
                    show: true,
                },
                icon: {
                    src: '/img/flylineChart/mapCenterPoint.png',
                    width: 30,
                    height: 30
                },
                text: {
                    show: false
                }
                },
                {
                name: 'Somewhere',
                coordinate: [0.52, 0.23]
                },
                {
                name: 'Somewhere1',
                coordinate: [0.62, 0.55],
                halo: {
                    show: true,
                    color: '#8378ea'
                }
                },
            ],
            lines: [
                {
                source: 'Somewhere',
                target: 'Boston'
                },
                {
                source: 'Somewhere1',
                target: 'Boston',
                color: '#fb7293',
                width: 2
                },
            ],
            text: {
                show: true,
            },
            icon: {
                show: false,
                src: './img/Massachusetts.png'
            },
            k: 0.5
        }
    })
}
</script>

<style lang="less">
#map {
  width: 100%;
  height: 100%;
  position: relative;
  box-shadow: 0 0 3px blue;
  display: flex;
  flex-direction: column;
  background-color: rgba(6, 30, 93, 0.5);
  border-top: 2px solid rgba(1, 153, 209, .5);
  box-sizing: border-box;
}
.bgimg{
    
  background-image: url('./img/Massachusetts.png') !important;
}
</style>
