<template>
  <div id="app">
    <binary-clock class="bclock"></binary-clock>
  </div>
</template>

<script>
import BinaryClock from "@/components/BCDClock";

export default {
  name: 'App',
  components: {BinaryClock}

}
</script>

<style>
#app {

}
.bclock {
  border-radius: .5rem;
}
</style>
