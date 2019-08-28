<template>
  <div class="father">
    这里是father父组件
    <p>这是从root组件的provide中获取的数据rootA:{{rootA}}</p>
    <p>这是从root组件的provide中获取的数据rootNum:{{rootNum}}</p>
    <b>{{$parent.rootA}}</b>
    <slot></slot>
  </div>
</template>

<script>
export default {
  data () {
    return {

    };
  },
  inject:["rootA","rootNum","rootFun"],
  components: {},

  computed: {},

  mounted () {},

  methods: {}
}
</script>

<style lang='scss' scoped>
</style>