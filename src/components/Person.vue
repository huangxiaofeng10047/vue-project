<template>
  <div class="person">
    <h1>{{ name }}</h1>
    <p>Age: {{ age }}</p>
    <button @click="changeName">修改名称</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">查看联系方式</button>
  </div>
</template>
<!-- <script lang="ts">
import { textChangeRangeIsUnchanged } from 'typescript';

 export default {
  name: 'Person',


 }

</script> -->

<script lang="ts" setup name="Person1234">

import { ref } from 'vue';
    //variables

let name = ref('张三');
    let age = ref(18);
    let tel = '1234567890';
    //methods
    function changeName() {
      name.value = '李四';
    }
    function changeAge() {
      age.value = 20;
    }
    function showTel() {
      alert(tel);
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
