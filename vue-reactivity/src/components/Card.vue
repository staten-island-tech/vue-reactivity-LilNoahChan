<template>
  <div class="Card">
<h2>{{ itemName }}</h2>
<img src="" alt="">
<p>{{ itemCost }}</p>
  </div>
</template>

<script>
  export default {
    name: 'Card'
    props: {
    section: String,
    itemName: String,
    itemCost: STring,
    },
  };
</script>

<style>
.card{
  width: 30%;
  background-color: red;
  height: 500px;
}
</style>