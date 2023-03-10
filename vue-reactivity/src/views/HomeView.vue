<script>
export default {
  name: "Home",
  components: {},
  data(){
    return{
      student: "Harry",
      graduated: false,
      animals: ["Pig", "Horse", "Donkey", "Cow", "Duck"]
    }
  }
}
</script>

<template>
<div class="home">
  <h1 v-if="graduated">{{student}}</h1>
  <h1 v-else>"They didnt gradate"</h1>
  <ul>
    <li v-for="animal in animals" :key="animal">{{ animal }}</li>
  </ul>

</div>
</template>

<style>
h1{
  color: red;
}
</style>