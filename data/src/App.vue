<template>
  <div id="app">
    {{ totalPriceMethod() }}
    {{ totalPriceMethod() }}
    {{ totalPrice }}
    {{ totalPrice }}
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      price: 1,
      number: 1,
    };
  },
  methods: {
    totalPriceMethod() {
      console.log("method");
      return this.number * this.price;
    },
  },
  computed: {
    totalPrice() {
      console.log("computed");
      return this.number * this.price;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
.active {
  border: 1px solid red;
}
[v-cloak] {
  display: none;
}
</style>
