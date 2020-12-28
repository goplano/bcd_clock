<template>
  <div class="panel">
    <light :value="pos3"></light>
    <light :value="pos2"></light>
    <light :value="pos1"></light>
    <light :value="pos0"></light>
  </div>
</template>

<script>
import Light from './Light'
export default {
  name: "LightPanel",
  components: {Light},
  props: {
    value: {
      type: Number,
      default: 0
    }
  },
  computed: {
    pos0() {
      return this.value & 1;
    },
    pos1() {
      return this.value & 2;
    },
    pos2() {
      return this.value & 4;
    },
    pos3() {
      return this.value & 8;
    },
  }
}
</script>

<style scoped>
.panel {
  display: flex;
  flex-direction: column;
  justify-items: flex-start;
}
</style>