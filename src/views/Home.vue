<template>
  <div>
    <HamburgerMenu></HamburgerMenu>
    <HomeTop></HomeTop>
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
import HomeTop from "../components/HomeTop.vue"

export default {
  components: {
    HomeProfile,
    HomeSkill,
    HomeWork,
    HamburgerMenu,
    HomeTop
  }
}
</script>