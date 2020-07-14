<template>
<div class='app'>
<router-link to="/">Home</router-link>
<router-view />
<ConnectivityExample />
<vue-snotify></vue-snotify>
</div>
</template>

<script>
import ConnectivityExample from './components/ConnectivityExample'
export default {
  name: 'app',
  components: {
    ConnectivityExample
  }
}
</script>

<style>
.app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
