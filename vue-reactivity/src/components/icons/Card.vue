<template>
  <div class="card">
    
    <h2>{{ name }}</h2>

    <img :src="image" alt="" />

    <p>Cost: ${{ cost }}</p>

    <addList @button-click="addToList()"> Add {{ name }} to list ${{ cost }} </addList>
  </div>
</template>

<script>
import addList from "./addList.vue";

  export default {
    name: "Card",
    props: {
      name: String,
      cost: Number,
      image: String,
    },

    components: {
      addList,
    },

    methods: {
      addToList() {
        this.$emit('addToList', {product: this.name, cost: this.cost})
      }
    }
  };
</script>

<style>
button {
  width: 100px;
  height: 100px;
}
.card {
  height: fit-content;
  display: flex;
  flex-direction: column;
  padding: 1rem 1rem 2rem;
  background: #f8f3e8;
  box-shadow: 0 0 40px rgba(0, 0, 0, 0.2), 0 0 40px rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  margin-bottom: 30px;
  width: fit-content;
  align-items: center;
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
