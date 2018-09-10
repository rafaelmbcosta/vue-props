<template lang="html">
  <div>
    Server #{{ server.id }} <button @click="selectedServer">Select</button>
  </div>
</template>

<script>
import { serverBus } from './main';

export default {
  props: ['server'],
  methods: {
    selectedServer(){
      serverBus.$emit('pamonha', this.server);
    }
  }

}
</script>

<style lang="css">
</style>
