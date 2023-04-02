<template>
    <div>
        <div v-show="listitems" class="listitems">
      <h2 class="name">{{ name }}</h2>
      <img src="image" alt="" />
      <p>{{ cost }}</p>
      <removefromCartButton @click="listitems = !listitems">
        Remove {{ name }} from Cart ${{ cost }}
      </removefromCartButton>
    </div>
    </div>
</template>

<script>
import removeList from './removeList.vue';


export default{
    name: "List",
    props:{
        name: String,
        cost: Number,
        image: String,
    },
    data(){
        return{
            total: 1,
            listitems: true,
        };
    },
    components: {
        removeList,
    },
    methods: {},
};
</script>

<style scoped>
  button{
  width: 200px;
  font-size: 15px;
  border: 10px white;
  border-radius: 50px;
  }
</style>