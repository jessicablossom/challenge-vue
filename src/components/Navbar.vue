<template>
  <nav>
    <div class="logo">
      <img src="https://challenge-api.aerolab.co/design/assets/Combined%20Shape%202.png" />
      <span>
        <strong>Ez</strong>Shop
      </span>
      <div class="right">Monto $ 0,00</div>
      <img
        src="https://challenge-api.aerolab.co/design/assets/shopping-cart.png"
        height="22px"
        width="22px"
      />
      <p class="badge">1</p>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped>
nav {
  background-color: #ffffff;
  height: 50px;
  padding: 2px;
  margin-bottom: 15px;
}
img {
  margin-right: 20px;
}
.logo {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  font-size: 17px;
  color: #006de3;
  letter-spacing: -0.41px;
  line-height: 20px;
}
.right {
  margin: auto;
  align-self: flex-end;
}
.badge {
  position: absolute;
  margin: auto;
  right:1%;
  top:1%;
  width: 21px;
  height: 21px;
  background: #0070e0;
  border: 1px solid #ffffff;
  color: #ffffff;
  border-radius: 50%;
  font-size: 8px;
  color: #ffffff;
  letter-spacing: -0.19px;
}
</style>