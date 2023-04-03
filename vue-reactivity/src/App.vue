<template>
  <header>
    <h1>CVS SHOPPING LIST</h1>
  </header>
  
  <main>
    <div class="container">
      <div class="home">
        <Card
          v-for="thing in items"
          :key="thing.name"
          :name="thing.name"
          :cost="thing.cost"
          :image="thing.img"
          @addToList="addToList"
        />
      </div>
      <div class="list">
        <h1>LIST</h1>
        <li v-for="item in list" :key="item">
          {{ item.product }} - ${{ item.cost }}
        </li>
        <p>Total: ${{ total }}</p>
      </div>
    </div>
  </main>
</template>

<script>
import { items } from "./assets/items.js";
import addList from "./components/icons/addList.vue";
import Card from "./components/icons/Card.vue";

export default {
  data() {
    return {
      items,
      list: [],
      total: 0,
    };
  },
  methods: {
    addToList({ product, cost }) {
      this.list.push({ product, cost });
      this.total+=cost
      console.log(this.list);
    },
  },
  components: {
    addList,
    Card,
  },
};
</script>

<style>
header{
  margin-bottom: 30px;
}
.container {
  display: flex;
}
.home {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  width: 75%;
}
h1 {
  position: relative;
  padding: 0;
  margin: 0;
  text-align: center;
  font-family: "Raleway", sans-serif;
  font-weight: 300;
  font-size: 40px;
  color: #080808;
}


.list{
  font-size: 2.5rem;
  background-color: antiquewhite;
  border-radius: 30px;
  border: #080808;
  margin-left: 1rem;
  align-content: center;
  align-items: center;
}
</style>
