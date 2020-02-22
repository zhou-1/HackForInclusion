<template>
  <div class="pointChart">
    <div class="title">Data Title</div>
    <!-- full demo here: https://emiliorizzo.github.io/vue-d3-network/ -->
    <d3-network :net-nodes="nodes" :net-links="[]" :options="options" />
    <!--div class="controls">
        <label>Force: {{force}}</label>
        <input type="range" min="-500" max="500" v-model="force"> 
        <label>Forces X: {{fX}}</label>
        <input type="range" min="0" max="1" step=".01" v-model="fX"> 
        <label>Forces Y: {{fY}}</label>
        <input type="range" min="0" max="1" step=".01" v-model="fY"> 
        
        <label class="in">Center:</label>
        <input type="checkbox" v-model="fC"> 
        <label class="in">Many Body:</label>
        <input type="checkbox" v-model="fMb"> 
        <button v-on:click="reset">
            restart simulation
        </button>
    </div-->
  </div>
</template>

<script>
import D3Network from 'vue-d3-network'
export default {
    name:"pointChart",
    components: {
        D3Network
    },
    data () {
        return {
        force:30,
        fX:0.5,
        fY:0.5,
        fMb:true,
        fC:true,
        nNodes:300
        }
    },

        computed:{
    nodes(){
        return this.makeNodes()
    },
    options(){
        return {
            force: this.force,
            forces:{
            X:this.fX,
            Y:this.fY,
            ManyBody:this.fMb,
            Center: this.fC,
            
        },
        nodeSize: 20,
        nodeLabels: false
        }
    }
    },
    methods:{
        makeNodes(){
            return Array.apply(null, { length: this.nNodes }).map((value, index) => { return {id:index, _color:this.randomColor(),_size:Math.random() * 30}})
        },
            reset(){
            this.nNodes++
        },
        randomColor () {
        return 'rgb(' + parseInt( Math.random()*64) +1 + ',' + parseInt( Math.random()*10) + 1+ ',' + 100 + ')'
        }
    }
}
</script>

<style>
.pointChart{
  background-color: rgba(6, 30, 93, 0.5);
  border-top: 2px solid rgba(1, 153, 209, .5);
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  
}
.title {
    padding-top: 1vh;
    height: 10%;
    font-weight: bold;
    text-indent: 20px;
    font-size: 20px;
    align-items: center;
  }
.net{
    height: 80%;
    width: 100%;
}
</style>