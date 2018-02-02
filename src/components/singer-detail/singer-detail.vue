<template>
  <transition name="slider">
    <div class="singer-detail"></div>
  </transition>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters([
      'singer'
    ])
  },
  created() {
    console.log(this.singer)
  }
}
</script>

<style lang="stylus" scoped>
  @import "~common/stylus/variable"

  .singer-detail 
    position: fixed
    z-index: 100
    top: 0
    left: 0
    right: 0
    bottom: 0
    background: $color-background

  .slider-enter-active, .slider-leave-active 
    transition: all 0.3s
  .slider-enter, .slider-leave
    transform: translate3d(100%, 0, 0)
</style>
