<template>
  <div id="app">
    <button @click="qh()">web前端</button>
    <button @click="qh1()">php工程师</button>
    <my-my :class="{'display':active1}"></my-my></br>
    <my-my2 :class="{'display':active2}"></my-my2>

  </div>
</template>



<script>
import myMy from './components/my';
import myMy2 from './components/my2';

export default {
  name: 'app',
  components: {
    myMy,
    myMy2,
  },
  data(){
    return{
        active1:false,
        active2:true
    }
  },
  methods:{
    qh:function(){
      this.active1=false,
      this.active2=true
    },
      qh1:function(){
      this.active1=true,
      this.active2=false
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.display{
  display:none;
}
button{
  font-size: 15px;
  border-radius: 15px;
  background: cornflowerblue;
  color: white;
}
</style>
