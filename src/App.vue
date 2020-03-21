<template>
  <div>
    <!-- <a class="menu-trigger" v-on:click="isactive=!isactive" v-bind:class='{active:isactive}' href="#">
      <span></span>
      <span></span>
      <span></span>
    </a> -->
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isactive: false
    }
  }
  
}
</script>

<style>
  .menu-trigger,
  .menu-trigger span {
    display: inline-block;
    transition: all .4s;
    box-sizing: border-box;
  }
  .menu-trigger {
    position: relative;
    width: 50px;
    height: 44px;
  }
  .menu-trigger span {
    position: absolute;
    left: 0;
    width: 100%;
    height: 4px;
    background-color: #111;
    border-radius: 4px;
  }
  .menu-trigger span:nth-of-type(1) {
    top: 0;
  }
  .menu-trigger span:nth-of-type(2) {
    top: 20px;
  }
  .menu-trigger span:nth-of-type(3) {
    bottom: 0;
  }
  .menu-trigger.active span:nth-of-type(1) {
    transform: translateY(20px) rotate(-135deg);
  }
  .menu-trigger.active span:nth-of-type(2) {
    opacity: 0;
  }
  .menu-trigger.active span:nth-of-type(3) {
    transform: translateY(-20px) rotate(135deg);
  }
</style>