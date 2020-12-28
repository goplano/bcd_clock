<template>
  <div class="number">
    <light-panel class="panel" :value="tens"></light-panel>
    <light-panel  class="panel" :value="ones"></light-panel>
  </div>
</template>

<script>
import LightPanel from "@/components/LightPanel";

export default {
  name: "ClockNumber",
  props: {
    value: {
      type: Number,
      default: 0
    }
  },

  components: {LightPanel},
  mounted() {

  },
  computed: {
    tens() {
      return this.value / 10
    },
    ones() {
      return this.value % 10
    }
  }
}
</script>

<style scoped>
.number {
  display: flex;
  margin: 5px;

justify-content: center;

}
.panel {
  flex: 0
}
</style>