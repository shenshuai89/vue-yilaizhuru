<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Root>
      <Father>
        <Son>
          <Grandson></Grandson>
        </Son>
      </Father>
    </Root>
  </div>
</template>

<script>
import Root from "./components/Root.vue"
import Father from "./components/Father.vue"
import Son from "./components/Son.vue"
import Grandson from "./components/Grandson.vue"
export default {
  name: 'app',
  components: {
    Root,Father,Son,Grandson
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
