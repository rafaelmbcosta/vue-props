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
            <app-detail></app-detail>
        </div>
        <hr>
        <app-footer></app-footer>
    </div>
</template>

<script>
  import Header from './Header'
  import Footer from './Footer'
  import Detail from './Detail'
  import ServerList from './ServerList'

  export default{
    components: {
      'app-header': Header,
      'app-footer': Footer,
      'app-detail': Detail,
      'app-server-list': ServerList
    }
  }

</script>

<style>

</style>
