<template>
  <Navbar></Navbar>
  <div class="mt-8"></div>
  <router-view></router-view>
</template>

<script>
import Navbar from '@/components/NavbarComp.vue'
export default {
  components: {Navbar},
};
</script>

<style>

</style>