<template>
  <div id="app">
    <div class="header" >
      <div class="title">EMBOLIUS</div>
      <div class="substitle">A card game...</div>
      </div>

    <div class="playgound">
<div class="playerhp">ENEMY: {{ enemyPts }}</div>
      <div class="enemyCards">
        <div class="enemyCard1 card"></div>
        <div class="enemyCard2 card"></div>
        <div class="enemyCard3 card"></div>
    </div>
     <div class="myCards">
        <div class="myCard1 card"></div>
        <div class="myCard2 card"></div>
        <div class="myCard3 card"></div>
    </div>
<div class="playerhp">YOU: 0</div>
<div class="handlehands">
    <appMyHand  />
</div>
    </div>
    <div class="bot">By Ager</div>
  </div>
</template>

<script>
import appMyHand from './components/MyHand.vue';
export default {
  components:{
    appMyHand
  },
  data(){
    return{
      enemyPts: 5
    }
  }
 
  
}
</script>
<style lang="scss">
@import "./assets/sass/main.scss";

.playgound{
  padding-left: 18%;
  padding-right: 18%;
}
.playerhp{ 
  text-align: center;
  font-size: 20px;
  color: color("accent");
}
.enemyCards{
  display: inline-block;
}
.myCards{
  display: block;
}

.card{
  height: 150px;
  width: 75px;
  background-color: lightsalmon;
  border: 1px black solid;
  border-radius: 10px;
  float: left;
}
.handlehands{
  position: relative;
  .handcard{
    position: absolute;
    height: 150px;
    width: 75px;
    background-color: lightsalmon;
    border: 1px black solid;
    border-radius: 10px;
    text-align: center;
  }
}
.header{
    border-bottom: black 1px solid;
    background-color: color('foreground');
    text-align: center;
  .title{
    color: color('primary');
    font-size: 24px;
  }
  .substitle{
    font-size: 12px;
    color: color('secondary');
  }
}


.bot{
  border-top: black 1px solid;
  background-color: color('foreground');
  position: absolute;
  width: 100%;
  bottom: 0px;
  text-align: center;
}

</style>
