<template>
  <div class="container">
    <app-header></app-header>
    <main>
      <router-view> </router-view>
    </main>
  </div>
</template>

<script>
import Header from './components/Header.vue';
export default {
  created(){
    this.$store.dispatch('initStocks');
  },
  components: {
    appHeader: Header,
  }
} ;
</script>

<style>
  body{
    padding:30px;
  }
</style>
