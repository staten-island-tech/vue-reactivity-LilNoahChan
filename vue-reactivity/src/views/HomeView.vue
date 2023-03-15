<script>
export default {
  name: "Home",
  components: {},
  data(){
    return{
      selected: "",
      // loggedIn: false,
      // student: "Harry",
      // graduated: true,
      // animals: ["Pig", "Horse", "Donkey", "Cow", "Duck"]
    };
  },
  computed:{
    now: function(){
      const time = new Date();
      return `${time.getHours}:${time.getMinutes}`;
    },
  },
  methods: {},
  // methods: {
  //   authState: function () {
  //     if(this.loggedIn===false){
  //       this.loggedIn = true;
  //     } else {
  //       this.loggedIn = false;
  //     }
  //   },
  // },
};
</script>

<style>
button {
  font-size: 30px;
}
</style>

<template>
  <div class="home">
    <h2>{{ now }}</h2>
  </div>
  <!-- <div class="home">
    <select v-model="selected">
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>
  <span>{{ selected }}</span>
  </div> -->

  <!-- <div class="home">
    <input type="text" placeholder="edit me" v-model="message" />
    <p>{{ message }}</p>
  </div> -->

  <!-- <div class="home">
    <button v-on:click="authState" v-if="loggedIn">Log Out</button>
    <button @click="authState" v-else>Login</button>
  </div> -->

<!-- <div class="home">
  <h1 v-if="graduated">{{student}}</h1>
  <h1 v-else>"They didnt gradate"</h1>
  <ul>
    <li v-for="animal in animals" :key="animal">{{ animal }}</li>
  </ul>

</div> -->
</template>

<style>
h1{
  color: red;
}
</style>