<template>
  <input class="input" type="text" placeholder="Search..." />
  <Slider />
  <Slider />
  <Slider />
  <Slider />
  <Slider />
  <Slider />
</template>

<script>
import Slider from "@/components/Slider.vue";
export default {
  components: {
    Slider
  }
};
</script>

<style lang="scss" scoped>
.input {
  z-index: 2;
  top: 0;
  left: 0;
  position: fixed;
  width: 100%;
  height: 45px;
  background: #ffffff;
  border: 4px solid #a8abbb;
}
</style>
