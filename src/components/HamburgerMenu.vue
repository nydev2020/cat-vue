<template>
  <div>
    <button class="button" type="button" name="button" v-on:click="active=!active">
      <span class="top" v-bind:class="{active:active}"></span>
      <span class="middle" v-bind:class="{active:active}"></span>
      <span class="bottom" v-bind:class="{active:active}"></span>
    </button>
    <transition>
      <nav id="gnav" class="nav" v-show="active">
        <div class="nav__body">
          <ul class="nav__list">
            <li class="nav__item"><a href="#">Home</a></li>
            <li class="nav__item"><a href="#about">About</a></li>
            <li class="nav__item"><a href="#skill">Skill</a></li>
            <li class="nav__item"><a href="#work">Work</a></li>
            <li class="nav__item">Post</li>
            <li class="nav__item"><router-link to="/" tag="a">Profile</router-link></li>
            <li class="nav__item"><router-link to="/users" tag="div">Users</router-link></li>
          </ul>
        </div>
      </nav>
    </transition>
  </div>
</template>


<script>
export default {
  data() {
    return {
      active: false
    }
  }
}
</script>

<style lang="scss" scoped>
  button {
    display: block;
    width: 50px;
    height: 50px;
    background-color: transparent;
    border: none;
    position: relative;
    position: fixed;
    z-index: 100;
    appearance: none;
    cursor: pointer;
    outline: none;
    span {
      display: block;
      width: 20px;
      height: 2px;
      margin: auto;
      background: #000;
      position: absolute;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      transition: .5s ease;
      &.top {
        transform: translateY(-6px)
      }
      &.bottom {
        transform: translateY(6px)
      }
    }
  }
  .nav {
    width: 20%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    background: #fffddd;
    &__body {
      padding: 40px;
    }
    &__list {
      list-style: none;
    }
    &__item {
      cursor: pointer;
      font-size: 1.5rem;
      line-height: 2;
      position: relative;
      display: table;
      a {
        text-decoration: none;
        color: #333;
      }
      &::after {
        position: absolute;
        bottom: 10px;
        left: 0;
        content: '';
        width: 100%;
        height: 2px;
        background: #333;
        opacity: 0;
        visibility: hidden;
        transition: .5s;
      }
      &:hover::after {
        bottom: 0px;
        opacity: 1;
        visibility: visible;
      }
    }
  }
  .top.active{
    transform: rotate(135deg);
  }
  .middle.active {
    opacity: 0;
  }
  .bottom.active {
    transform: rotate(-135deg);
  }
  .v-enter, .v-leave-to {
    opacity: 0;
  }
  .v-enter-active, .v-leave-active {
    transition: .5s;
    position: absolute;
  }
</style>