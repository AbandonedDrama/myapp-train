<template>
  <div id="app">
    <myHeader></myHeader>
    <!-- 路由匹配到的组件将渲染在这里 -->
    <transition name="fade" mode="out-in">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
import myHeader from './components/header/myHeader.vue'
export default {
  name: 'app',
  data () {
    return {}
  },
  methods: {},
  components: { myHeader }
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
  }
  html, body, #app{
    width: 100%;
    height: 100%;
  }
  .fade-enter-active, .fade-leave-active {
    transition: opacity .5s
  }
  .fade-enter, .fade-leave-active {
    opacity: 0
  }
</style>
