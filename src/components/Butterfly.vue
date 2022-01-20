<template>
  <div class="model">
    <model-gltf
      :scale="scale"
      :position="position"
      :rotation="rotation"
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
      position: {
        x: 0,
        y: 0,
        z: 0,
      },
      scale: {
        x: 1,
        y: 1,
        z: 1,
      },
      rotation: {
        x: 0,
        y: 0,
        z: 0,
      },
      bgColor: "#ff0",
      bgAlpha: 0.1,
    };
  },
  methods: {
    setPositionHead() {
      this.position.x = -40;
      this.position.y = -420;
      this.scale.x = 3;
      this.scale.y = 3;
      this.scale.z = 3;
      this.rotation.x = 0.02;
      this.rotation.y = 0.5;
      this.rotation.z = -0.09;
    },
    setPositionBehind() {
      this.position.x = 0;
      this.position.y = 0;
      this.scale.x = 1;
      this.scale.y = 1;
      this.scale.z = 1;
      this.rotation.x = 0;
      this.rotation.y = 3.2;
      this.rotation.z = 0;
    },
    setPositionLeg() {
      this.position.x = 10;
      this.position.y = 40;
      this.scale.x = 2.5;
      this.scale.y = 2.5;
      this.scale.z = 2.5;
      this.rotation.x = 0;
      this.rotation.y = 0;
      this.rotation.z = 0;
    },
    ResetPosition() {
      this.position.x = 0;
      this.position.y = 0;
      this.scale.x = 1;
      this.scale.y = 1;
      this.scale.z = 1;
      this.rotation.x = 0;
      this.rotation.y = 0;
      this.rotation.z = 0;
    },
  },
  components: {
    ModelGltf,
  },
};
</script>

<style>
</style>