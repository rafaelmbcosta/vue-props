<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
              <app-header></app-header>
            </div>
        </div>
        <hr>
        <div class="row">
            <app-server-list></app-server-list>
            <app-panel></app-panel>
        </div>
        <hr>
        <app-footer></app-footer>
    </div>
</template>

<script>
  import Header from './Header'
  import Footer from './Footer'
  import Panel from './Panel'
  import ServerList from './ServerList'

  export default{
    components: {
      'app-header': Header,
      'app-footer': Footer,
      'app-panel': Panel,
      'app-server-list': ServerList
    }
  }

</script>

<style>

</style>
