<template>
  <div>
    <div class="header1">
      <p>Quanment</p>
      <p>History</p>
    </div>
    <div class="header2">Welcome to Quantity Measurment</div>
  </div>
</template>

<script>
export default {
  name: "AppBar",
};
</script>

<style >
.header1 {
  background-color: #f5f6fa;
  height: 50px;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.header2 {
  background-color: #446dff;
  width: 100%;
  height: 75px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: left;
  font: normal normal normal 25px/30px Montserrat;
  letter-spacing: 0px;
  text-transform: capitalize;
}
</style>