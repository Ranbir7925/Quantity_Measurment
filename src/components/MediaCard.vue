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
  justify-content: center;
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
  border-radius: 7px;
}
.length:hover{
  background-color: #edfdf9;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #0ec098;
  color: #0ebe98;
}
.temperature:hover {
  background-color: #ffeef0;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #fd5160;
  color: #fd5160;
}
.volume:hover {
  background-color: #e8ddff;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #7224ff;
  color: #7224ff;
}
.data {
  height: 25%;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>