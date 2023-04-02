<template>
    <button><slot></slot></button>
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
  
  <style scoped>
  
  </style>