<template>
  <div class="clock">
    <clock-number class="digit" :value="hours"></clock-number>
    <clock-number class="digit" :value="minutes"></clock-number>
    <clock-number class="digit" :value="seconds"></clock-number>
  </div>
</template>

<script>
import ClockNumber from "@/components/ClockNumber";

export default {
  name: "BCDClock",
  components: {
    ClockNumber
  },
  data() {
    return {
      time: null
    }
  },
  methods: {
    getTime() {
      this.time = new Date();
    }
  },
  created() {
    this.getTime()
  },
  mounted() {
    setInterval(this.getTime.bind(this), 1000);
  },
  computed: {
    hours() {
      return this.time.getHours()
    },
    minutes() {
      return this.time.getMinutes()
    },
    seconds() {
      return this.time.getSeconds()
    }
  }
}
</script>

<style scoped>
.clock {
  display: flex;
  height: 100%;
  width: 300px;
  background-color: #2c3e50;
}
.digit {
  flex:1;
  height: 100%;
}
</style>