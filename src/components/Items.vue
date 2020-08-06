<template>
  <div class="grid">
    <div class="card" v-bind:key="item.id" v-for="item in items">
      <img :src="item.photo" height="148px" width="148px" />
      <p class="name">{{item.name}}</p>
      <p class="price">$ {{item.price}}</p>
      <button class="btn secondary">Agregar al Carrito</button>
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
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  background-color: #ffffff;
  border-radius: 3px;
  box-shadow: 5px 5px 5px 0px #00000008 ;
  margin-bottom: 30px;
  margin-right: 2px;;
  padding: 10px;
  width: 180px;
  height: auto;
}

.secondary {
  background: #ffffff;
  border: 1px solid #0070e0;
  color: #0070e0;
  }

.secondary:hover {
  background-color: #0070e0;
  border: 1px solid transparent;
  color: #ffffff;
}

</style>



