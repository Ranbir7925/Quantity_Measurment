<template>
  <div class="outter">
    <div class="card-container">
      <p>CHOOSE TYPE</p>

      <div class="selection-container">
        <div class="length" @click="isActive('length')" v-bind:class="{'length-selected': selected == 'length'}">
          <img src="../assets/active_scale.svg" />
          <div class="data">Length</div>
        </div>
        <div class="temperature" @click="isActive('temperature')" v-bind:class="{'temperature-selected': selected == 'temperature'}">
          <img src="../assets/active_hot.svg" />
          <div class="data">Temperature</div>
        </div>
        <div class="volume" @click="isActive('volume')" v-bind:class="{'volume-selected': selected == 'volume' }">
          <img src="../assets/active_beaker.svg" />
          <div class="data">Volume</div>
        </div>
      </div>
    </div>
    <Textbox />
  </div>
</template>

<script>
import Textbox from "./Text";

export default {
  name: "MediaCard",
  components: {
    Textbox,
  },
  data(){
    return{
    selected: "length",
    }
  },
  methods: {
    isActive: function (type) {
      this.selected = type
    },
  },
};
</script>

<style scoped>
.outter {
  /* width: 100%; */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.card-container {
  margin-top: 20px;
  margin-bottom: 20px;
  width: 560px;
  display: flex;
  flex-direction: column;
  align-items: start;
  justify-content: center;
}
.selection-container {
  width: 100%;
  display: flex;
  justify-content: space-between;
}
.length,
.temperature,
.volume {
  filter: grayscale(100%);
  background: #ededed;
  border: 1px solid #ededed;
  flex-direction: column;
  display: flex;
  justify-content: center;
  width: 173px;
  height: 137px;
  border-radius: 7px;
}

.length:hover{
  filter: none;
  background-color: #edfdf9;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #0ec098;
  color: #0ebe98;
}

.length-selected{
  filter: none;
  background-color: #edfdf9;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #0ec098;
  color: #0ebe98;
}
.temperature:hover {
  filter: none;
  background-color: #ffeef0;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #fd5160;
  color: #fd5160;
}
.temperature-selected{
  filter: none;
  background-color: #ffeef0;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #fd5160;
  color: #fd5160;
}

.volume:hover {
  filter: none;
  background-color: #e8ddff;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #7224ff;
  color: #7224ff;
}

.volume-selected{
  filter: none;
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