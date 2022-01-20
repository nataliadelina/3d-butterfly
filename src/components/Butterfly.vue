<template>
  <div class="model">
    <model-gltf
      src="static/butterfly/scene.gltf"
      :backgroundAlpha="bgAlpha"
      :backgroundColor="bgColor"
    >
    </model-gltf>
    <div class="txt">
      <h1>beautiful butterfly</h1>
      <h2>3D</h2>
    </div>
  </div>
</template>

<script>
import { ModelGltf } from "vue-3d-model";

export default {
  data() {
    return {
      bgColor: "#ff0",
      bgAlpha: 0.1,
    };
  },

  components: {
    ModelGltf,
  },
};
</script>

<style>
</style>