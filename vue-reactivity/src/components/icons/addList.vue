<template>
  <button @click="$emit('button-click')"><slot></slot></button>
</template>

<script>
export default {
  name: "addList",
  data() {
    return {};
  },
  props: {
    name: String,
    cost: Number,
  },
  methods: {},
};
</script>

<style>
button {
  width: 200px;
  font-size: 15px;
  border: 10px white;
  border-radius: 50px;
  border: 2px black solid;
  cursor: pointer;
}
</style>
