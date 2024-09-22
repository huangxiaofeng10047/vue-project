<template>
  <div class="person">
    <h1>{{ name }}</h1>
    <p>Age: {{ age }}</p>
    <button @click="changeName">修改名称</button>
    <button @click="changeAge">修改年龄</button>
   
   </div>
</template>
<!-- <script lang="ts">
import { textChangeRangeIsUnchanged } from 'typescript';

 export default {
  name: 'Person',


 }

</script> -->

<script lang="ts" setup name="Person1234">
import { ref,reactive, toRefs } from 'vue';
    //variables

let person = reactive({
  name: 'John Doe',
  age: 30,
})
let {name,age}=toRefs(person)

function changeName() {
  name.value += '~';
}

function changeAge() {
  age.value +=1;
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
