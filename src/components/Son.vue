<template>
  <div class="son">
    这里是son儿组件
    <p>这是从root组件的provide中获取的数据rootA:{{rootA}}</p>
    <p>这是从root组件的provide中获取的数据rootNum:{{rootNum}}</p>
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