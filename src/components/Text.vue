<template>
  <div class="text-box">
    <div class="conversion-container">
      FROM
      <div class="input-container">
        <div class="value">
          <input type="text" class="textbox" />
        </div>
        <div class="unit">
          <select name="select-box" id="">
            <option value="">Kilometer</option>
            <option value="">Meter</option>
            <option value="">CentiMeter</option>
            <option value="">MiliMeter</option>
            <option value="">MicroMeter</option>
            <option value="">Mile</option>
            <option value="">Foot</option>
            <option value="">Inch</option>
          </select>
        </div>
      </div>
    </div>
    <div class="conversion-container">
      TO
      <div class="input-container">
        <div class="value">
          <input type="text" class="textbox" />
        </div>
        <div class="unit">
          <select name="select-box" id="">
            <option value="">Kilometer</option>
            <option value="">Meter</option>
            <option value="">CentiMeter</option>
            <option value="">MiliMeter</option>
            <option value="">MicroMeter</option>
            <option value="">Mile</option>
            <option value="">Foot</option>
            <option value="">Inch</option>
          </select>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Textbox",
  data() {
    return {
      selected: "",
    };
  },
};
</script>
<style scoped>
.text-box {
  width: 560px;
  display: flex;
  justify-content: space-between;
}
.input-container {
  display: flex;
  flex-direction: column;
  background-color: #ffffff;
  width: 260px;
  height: 96px;
}
.textbox {
  padding: 0 10px;
  font-size: larger;
  width: 100%;
  height: 50px;
  outline: none;
  background-color: #ededed;
  border: 0px solid #e7dcfe;
}
.unit select {
  padding: 0 10px;
  width: 100%;
  height: 35px;
  outline: none;
  background-color: #ededed;
  border: 1px solid #e7dcfe;
}

.select-box {
  max-width: 350px;
  height: 48px;
  border: 1px solid #e7dcfe;
  border-radius: 3px;
  padding: 15px 27px;
  font: normal normal normal 15px/19px Montserrat;
  text-transform: uppercase;
  -webkit-appearance: none;
  -moz-appearance: none;
}
</style>