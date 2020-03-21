<template>
  <div>
    <HamburgerMenu></HamburgerMenu>
    <h3>HOME</h3>
    <router-link to="/users">Users</router-link>
    <HomeProfile></HomeProfile>
    <HomeSkill></HomeSkill>
    <HomeWork></HomeWork>
  </div>
</template>

<script>
import HomeProfile from "../components/HomeProfile.vue";
import HomeSkill from '../components/HomeSkill.vue';
import HomeWork from "../components/HomeWork";
import HamburgerMenu from "../components/HamburgerMenu.vue";

export default {
  components: {
    HomeProfile,
    HomeSkill,
    HomeWork,
    HamburgerMenu
  }
}
</script>