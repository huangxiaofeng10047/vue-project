<template>
 
    <Person />

</template>

<script lang="ts">
import Person  from "./components/Person.vue";
export default {
  name: 'App',
  components: { //注册组建
    Person
  }
}
</script>



