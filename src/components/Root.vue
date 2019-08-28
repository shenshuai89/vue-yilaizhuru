<template>
  <div class="root">
    这是root根组件
    <p>这是root组件中的rootA{{rootA}}</p>
    <button @click="changeRootA">点击</button>
    <slot></slot>
  </div>
</template>

<script>
import { setInterval } from 'timers';
export default {
  data () {
    return {
        rootA:"rootA",
        rootNum:{
            a:10
        }
    };
  },
  provide(){
      return{
        rootA:this.rootA,
        rootNum: this.rootNum,
        rootFun:this.rootFun
    }
  },
  components: {},

  computed: {},
    created(){
        this.addRootNum()
        this.changeRootA()
    },
  mounted () {
      
  },

  methods: {
      rootFun(){
          console.log("rootA",this.rootA);
      },
      addRootNum(){
          setInterval(()=>{
            // 引用类型的数据，由于是引用的关系，在root中更新会对子孙组件有影响
            this.rootNum.a ++;
            // 基本数据类型，在root中改变后不会对子孙组件有影响。依赖注入提供的数据属于非响应式
            this.rootA = "改变之后的rootA数据"
          },1000)
      },
      changeRootA(){
          this.rootA = "改变之后的rootA数据"
      }
  }
}
</script>

<style lang='scss' scoped>
</style>