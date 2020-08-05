<template>
  <div class="grid">
    <div class="card" v-bind:key="item.id" v-for="item in items">
      <img :src="item.photo" height="148px" width="148px" />
      <p class="name">{{item.name}}</p>
      <p class="price">$ {{item.price}}</p>
      <button class="btn">Agregar al Carrito</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Items",
  props: ["items"],
};
</script>

<style scoped>
.name {
  font-size: 14px;
  line-height: 20px;
  text-align: center;
}
.price {
  color: #0070e0;
  font-size: 16px;
  font-weight: 600;
  text-align: center;
}
.grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}

div .card {
  background-color: #ffffff;
  border-radius: 3px;
  box-shadow: 5px 5px 5px 0px #00000008 ;
  margin-bottom: 30px;
  padding: 10px;
  width: 180px;
}

.btn {
  background: #ffffff;
  border: 1px solid #0070e0;
  border-radius: 3px;
  color: #0070e0;
  font-size: 13px;
  height: 32px;
  outline: none;
  text-align: center;
  width: 132px;
}

.btn:hover {
  background-color: #378de5;
  border: 1px solid transparent;
  color: #ffffff;
}

.btn:active {
  position: relative;
  top: 1px;
}
</style>



