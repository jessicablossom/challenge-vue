<template>
  <div id="app">
    <Navbar />
    <h1>Almacén</h1>
    <Items v-bind:items="items" />
    <LoadMore />
    <p>aca van mas productos</p>
  </div>
</template>

<script>
import Items from "./components/Items";
import Navbar from "./components/Navbar";
import LoadMore from "./components/LoadMore";
import axios from "axios";

export default {
  name: "app",
  components: {
    Items,
    Navbar,
    LoadMore,
  },
  data() {
    return {
      items: [],
    };
  },
  created() {
    axios
      .get("https://challenge-api.aerolab.co/products")
      .then((res) => (this.items = res.data.products))
      .catch((err) => console.log(err));
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  text-align: center;
  background: rgba(0, 0, 0, 0.05);
}
h1 {
  font-size: 24px;
  letter-spacing: 0;
  text-align: left;
  margin: 10px;
}
.btn {
  border-radius: 3px;
  font-size: 13px;
  height: 32px;
  outline: none;
  width: 132px;
  transition: ease-in-out 0.35s;
}
.btn:active {
  position: relative;
  top: 1px;
}

.primary {
  background: #0070e0;
  border: 1px solid #0070e0;
  color: #ffffff;
}
.primary:hover {
  background: #ffffff;
  border: 1px solid #0070e0;
  color: #0070e0;
}
</style>
