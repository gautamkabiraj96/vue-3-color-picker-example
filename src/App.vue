<template>
  <div>
    <div v-if="colors && Object.keys(colors).length !== 0" class="color-values">
      <h4>Color values:</h4>
      <p>{{ colors ? colors : "" }}</p>
    </div>
    <photoshop-picker v-model="colors" class="np-mb" />
    <compact-picker v-model="colors" class="np-mb" />
    <swatches-picker v-model="colors" class="np-mb" />
    <slider-picker v-model="colors" class="np-mb" />
    <sketch-picker v-model="colors" class="np-mb" />
    <chrome-picker v-model="colors" class="np-mb" />
    <material-picker v-model="colors" class="np-mb" />
  </div>
  <!--
    wwww.nightprogrammer.com
  -->
</template>

<script>
import {
  Photoshop,
  Material,
  Compact,
  Swatches,
  Slider,
  Sketch,
  Chrome,
} from "@lk77/vue3-color";

export default {
  name: "App",
  data() {
    return {
      colors: {},
    };
  },
  components: {
    "material-picker": Material,
    "compact-picker": Compact,
    "swatches-picker": Swatches,
    "slider-picker": Slider,
    "sketch-picker": Sketch,
    "chrome-picker": Chrome,
    "photoshop-picker": Photoshop,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.color-values {
  background: rgb(234, 226, 255);
  padding: 4px;
  max-width: 500px;
  margin: 0 0 30px 0;
  border: 1px solid rgb(76, 0, 255);
  min-height: 180px;
}

.np-mb {
  margin-bottom: 20px;
}

.color-values p {
  font-size: 14px;
}
</style>
