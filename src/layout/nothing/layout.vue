<template>
  <div>
    <router-view :key="routerViewKey" />
  </div>
</template>

<script>
// import { mapState, mapGetters, mapActions } from 'vuex'
// import mixinSearch from './mixins/search'
export default {
  name: 'layout-nothing',
  mixins: [],
  components: {},
  data () {
    return {}
  },
  computed: {
    /**
     * @description 用来实现带参路由的缓存
     */
    routerViewKey () {
      // 默认情况下 key 类似 __transition-n-/foo
      // 这里的字符串操作是为了最终 key 的格式和原来相同 类似 __transition-n-__stamp-time-/foo
      const stamp = this.$route.meta[`__stamp-${this.$route.path}`] || ''
      return `${stamp ? `__stamp-${stamp}-` : ''}${this.$route.path}`
    }
  },
  methods: {}
}
</script>

<style lang="scss">
</style>
