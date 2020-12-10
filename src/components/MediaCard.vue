<template>
  <div class="card-container">
    <p>CHOOSE TYPE</p>

    <div class="selection-container">
      <div class="length">
        <img src="../assets/scale.svg" />
        <div class="data">Length</div>
      </div>
      <div class="temperature">
        <img src="../assets/hot.svg" />
        <div class="data">Temperature</div>
      </div>
      <div class="volume">
        <img src="../assets/beaker.svg" />
        <div class="data">Volume</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MediaCard",
};
</script>

<style scoped>
.card-container p{
  flex-direction: column;
}
.selection-container {
  display: flex;
  justify-content: center;
}
.length,
.temperature,
.volume {
  margin: 1%;
  background: #ededed;
  flex-direction: column;
  display: flex;
  justify-content: center;
  width: 173px;
  height: 137px;
}
.data {
  height: 25%;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>