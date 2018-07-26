<template>
  <div id="app">
    <nav class="navbar navbar-default change_bg">
      <div class="container-fluid">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
          <a class="navbar-brand change_color" href="#">鸿合业务协作系统后台</a>
        </div>

        
      </div><!-- /.container-fluid -->
    </nav>
    <router-view></router-view>
  </div>
</template>

<script>
  export default{
    name: 'App'
  }
</script>
