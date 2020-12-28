<template>
  <div :class="classObject">

  </div>
</template>

<script>
export default {
  name: 'Light',
  props: {
    value: {
      type: Number,
      default: 0
    }
  },
  computed: {
    classObject() {
      return {
        'light': true,
          'on': this.value > 0
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.light {
  width: 20px;
  height: 20px;
  margin: 5px;
  min-height: 1rem;
  border-radius: 100px;
  background-color: rgba(200, 200, 200, 0.2);
  border: 1px solid transparent;
  box-shadow: inset 0px 0px 5px 5px rgba(200, 200, 200, 0.2);
}
.on {
  border: 1px solid darkgreen;
  background-color: greenyellow;
  box-shadow: 0px 0px 5px 5px rgba(0, 255, 0, 0.2);
}
</style>
