<template>
  <div class="person">
    <!-- <h1>{{ name }}</h1>
    <p>Age: {{ age }}</p>
    <button @click="changeName">修改名称</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">查看联系方式</button> -->
   <h2>汽车信息： 一辆{{ car.brand }}车，价值{{ car.price }}万</h2>
   <button @click="changePrice">修改汽车品牌</button>
   <h2>游戏信息：</h2>
   <ul>
     <li v-for="game in games" :key="game.id">{{ game.name }}</li>
     </ul>
     <button @click="changeFirst">修改第一个游戏</button>
  </div>
</template>
<!-- <script lang="ts">
import { textChangeRangeIsUnchanged } from 'typescript';

 export default {
  name: 'Person',


 }

</script> -->

<script lang="ts" setup name="Person1234">
import { idText } from 'typescript';
import { ref } from 'vue';
    //variables

let car=ref({
  brand:'奔驰',
  price:100
})

let games = ref([
  {id:'ays01',name:'王者荣耀'},
  {id:'ays02',name:'英雄联盟'},
  {id:'ays03',name:'绝地求生'},
])

function changePrice(){
  car.value.brand='宝马'
}
function changeFirst(){
  games.value[0].name='穿越火线'
}
</script>
<style scoped>
.person {
  color: red;
}
button {
  margin: 10px;
}
</style>
