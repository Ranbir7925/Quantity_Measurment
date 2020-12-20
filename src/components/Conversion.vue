<template>

  <div class="outter">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">

    <div class="card-container">
      <p>CHOOSE TYPE</p>

      <div class="selection-container">
        <div
          class="length"
          @click="isActive('length')"
          v-bind:class="{ 'length-selected': conversionSelected == 'length' }"
        >
          <img src="../assets/active_scale.svg" />
          <div class="data">Length</div>
        </div>
        <div
          class="temperature"
          @click="isActive('temperature')"
          v-bind:class="{ 'temperature-selected': conversionSelected == 'temperature' }"
        >
          <img src="../assets/active_hot.svg" />
          <div class="data">Temperature</div>
        </div>
        <div
          class="volume"
          @click="isActive('volume')"
          v-bind:class="{ 'volume-selected': conversionSelected == 'volume' }"
        >
          <img src="../assets/active_beaker.svg" />
          <div class="data">Volume</div>
        </div>
      </div>
    </div>
    <Textbox
      :selectedSubUnit="selectedSubUnit"
      :subUnitTo="subUnitTo"
      :subUnitFrom="subUnitFrom"
      :intialUnitValueTo="intialUnitValueTo"
      :intialUnitValueFrom="intialUnitValueFrom"
      :lengthUnits ="lengthUnits"
    />
  </div>
</template>

<script>
import Textbox from "./Text";

export default {
  name: "Conversion",
  components: {
    Textbox,
  },
  data() {
    return {
      conversionSelected: "length",
      subUnitTo: "Meter",
      subUnitFrom: "CentiMeter",
      intialUnitValueTo: 1,
      intialUnitValueFrom: 100,
      selectedSubUnit: [],
      lengthUnits: [
        "Kilometer",
        "Meter",
        "CentiMeter",
        "MiliMeter",
        "MicroMeter",
        "Mile",
        "Foot",
        "Inch",
      ],
      temperatureUnits: ["Celsius", "Farhanite", "Kelvin"],
      volumeUnits: ["Liters", "MiliLiters", "Gallons"],
    };
  },
  methods: {
    isActive: function (type) {
      this.conversionSelected = type;
      if (type == "length") {
        this.selectedSubUnit = this.lengthUnits;
        this.subUnitTo = "Meter";
        this.subUnitFrom = "CentiMeter";
        this.intialUnitValueTo = 1;
        this.intialUnitValueFrom = 100;
      }
      if (type == "temperature") {
        this.selectedSubUnit = this.temperatureUnits;
        this.subUnitTo = "Celsius";
        this.subUnitFrom = "Farhanite";
        this.intialUnitValueTo = 0;
        this.intialUnitValueFrom = 32;
      }
      if (type == "volume") {
        this.selectedSubUnit = this.volumeUnits;
        this.subUnitTo = "Liters";
        this.subUnitFrom = "MiliLiters";
        this.intialUnitValueTo = 1;
        this.intialUnitValueFrom = 1000;
      }
    },
  },
};
</script>

<style >
.outter {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.card-container {
  margin-top: 20px;
  margin-bottom: 30px;
  width: 560px;
  display: flex;
  flex-direction: column;
  align-items: start;
  justify-content: center;
}
.selection-container {
  margin-top: 15px;
  width: 100%;
  display: flex;
  justify-content: space-between;
}
@media screen and (max-width: 600px) {
  .card-container {
    display: flex;
    flex-direction: row;
    align-items: start;
    justify-content: center;
  }
  .selection-container {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
  }
}
.length,
.temperature,
.volume {
  transition: 0.5s ease;
  filter: grayscale(100%);
  background: #ffffff;
  border: 1px solid #ffffff;
  flex-direction: column;
  display: flex;
  justify-content: center;
  width: 173px;
  height: 137px;
  border-radius: 7px;
}
.length:hover,
.length-selected {
  transition: 0.5s ease;
  filter: none;
  background-color: #edfdf9;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #0ec098;
  color: #0ebe98;
}
.temperature:hover,
.temperature-selected {
  transition: 0.5s ease;
  filter: none;
  background-color: #ffeef0;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #fd5160;
  color: #fd5160;
}
.volume:hover,
.volume-selected {
  transition: 0.5s ease;
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