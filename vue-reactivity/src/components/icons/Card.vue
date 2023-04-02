
<template>
<div class="card">
  <h2> {{name}}</h2>
  <img :src="image" alt="">
  <p>Cost: ${{ cost }}</p>
  <addList @click="click">
  Add {{ name }} to list ${{ cost }}
  </addList>
</div>
</template>

<script>
import addList from "./addList.vue";
import {store} from "./store.js";

export default{
  name: "Card",
  props: {
    name: String,
    cost: Number,
    image: String,
  },
  data(){
    return{
      store,
    };
  },
  components: {
    addList,
  },
  methods: {
    
  }

}
</script>


<style scoped>
button{
  width: 100px;
  height: 100px;
}
.card {
  height: fit-content;
  display: flex;
  flex-direction:column ;
  padding: 1rem 1rem 2rem;
  background: #f8f3e8;
  box-shadow: 0 0 40px rgba(0, 0, 0, 0.2), 0 0 40px rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  margin-bottom: 30px;
}

.card > img {
  width: 100%;
  height: auto;

}

.card > h2 {
  margin-top: 1rem;
  font-family: "Kalam", cursive;
  font-weight: normal;
  font-size: 2rem;
  color: #4a4a7d;
  text-align: center;
}

.card > p {
  font-family: "Kalam", cursive;
  font-size: 1rem;
  color: #5e5e89;
  text-align: center;
}

</style>