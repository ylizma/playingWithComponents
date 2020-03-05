<template>
  <div id="app">
    <navbar></navbar>
    <Rockets class="container" />
  </div>
</template>

<script>
import Rockets from '@/views/Rockets.vue';
import navbar from '@/components/Navbar.vue';
export default {
  name: 'App',
  components: {
    Rockets,
    navbar
  }
}
</script>

<style>

</style>
