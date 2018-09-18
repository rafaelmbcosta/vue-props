<template lang="html">
  <div>
    <p v-if="server"> Server <b>{{ server.id }}</b> selected, Server status: <b>{{ server.status }} </b></p>
    <button v-if="server" @click="resetServer"> Reset </button>
    <p v-else> Please select a server</p>
  </div>
</template>

<script>

import { serverBus } from './main';

export default {
  data: function() {
    return {
      server: null
    }
  },
  methods: {
    resetServer(){
      this.server.status = 'Normal';
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
