<template>
  <div id="app">
    <demo-main></demo-main>
  </div>
</template>

<script scope>
import { defineComponent } from 'vue'
import demoMain from './components/demo-main.vue'

export default defineComponent({
  name: 'App',
  components: { demoMain },
  setup() {
    return {}
  }
})
</script>

<style lang="less" scoped>
#app {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
