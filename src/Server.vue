<template lang="html">
  <div>
    Server #{{ id }} - {{ status }} <button @click="resetStatus">Reset Status</button>
  </div>
</template>

<script>
export default {
  props: ['id', 'status'],
  methods: {
    resetStatus: function(){
      this.status = 'Normal';
    }
  }
}
</script>

<style lang="css">
</style>
