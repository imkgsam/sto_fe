<template>
<div class="testing">
  <div>construction page</div>
  <flip-countdown deadline="2021-09-03 00:00:00"></flip-countdown>
</div>

</template>

<script>
import FlipCountdown from 'vue2-flip-countdown'
import { mapActions } from 'vuex'

export default {
  mixins: [],
  components: { FlipCountdown },
  data () {
    return {
    }
  },
  mounted () {},
  methods: {}
}
</script>

<style lang="scss">
  .testing{
    width:100vw;
    height:100vh;
  }
</style>
