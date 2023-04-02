
<template>
<div class="card">
  <h1></h1>
</div>
</template>

<script>
import addList from "./addList.vue";

export default{
  name: 'Card',
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
</style>