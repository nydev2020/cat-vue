<template>
  <div>
    <HamburgerMenu></HamburgerMenu>
    <h3>Users</h3>
    <router-link to="/">Home</router-link>
  </div>

</template>

<script>
import HamburgerMenu from '../components/HamburgerMenu.vue'

export default {
  components: {
    HamburgerMenu
  }
}
</script>

<style>

</style>