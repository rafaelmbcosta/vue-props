<template lang="html">
  <div>
    <p v-if="server"> Server #{{ server.id }} selected, Server status: {{ server.status }}</p>
    <p v-else> Please select a server</p>
  </div>
</template>

<script>
import { serverBus } from './main'

export default {
  data: function() {
    return {
      server: null
    }
  },
  created(){
    serverBus.$on('pamonha', (server) => {
      this.server = server;
    });
  }
}
</script>

<style lang="css">
</style>
