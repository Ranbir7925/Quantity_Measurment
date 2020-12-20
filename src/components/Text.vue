<template>
  <div class="text-box">
    <div class="conversion-container">
      FROM
      <div class="input-container">
        <input type="text" class="textbox" :value="intialUnitValueTo" />
        <div class="unit">
          <select v-model="subUnitTo">
            <option v-for="listValue in selectedSubUnit" :key="listValue">
              {{ listValue }}
            </option>
          </select>
        </div>
      </div>
    </div>
    <div class="conversion-container">
      TO
      <div class="input-container">
        <input type="text" class="textbox" :value="intialUnitValueFrom" />
        <div class="unit">
          {{ valuesList }}
          <select v-model="subUnitFrom">
            <option v-for="listValue in selectedSubUnit" :key="listValue">
              {{ listValue }}
            </option>
          </select>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Textbox",
  props: ["selectedSubUnit", "subUnitTo", "subUnitFrom", "intialUnitValueTo", "intialUnitValueFrom", "lengthUnits"],
  created() {
    this.loadDefault();
  },
  methods: {
    loadDefault() {
      this.selectedSubUnit = this.lengthUnits;
      this.subUnitTo = "Meter";
      this.subUnitFrom = "CentiMeter";
      this.intialUnitValueTo = 1;
      this.intialUnitValueFrom = 100;
    },
  },
};
</script>

<style >
.text-box {
  width: 560px;
  display: flex;
  justify-content: space-between;
}
.input-container {
  margin-top: 15px;
  display: flex;
  flex-direction: column;
  background-color: #ffffff;
  width: 260px;
}
.textbox {
  padding: 0 10px;
  font-size: larger;
  height: 50px;
  outline: none;
  background-color: #ffffff;
  border: 1px solid #f5f6fa;
}
.unit select {
  padding: 0 10px;
  width: 100%;
  height: 35px;
  outline: none;
  background-color: #ffffff;
  border: 1px solid #f5f6fa;
}
</style>