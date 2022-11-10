<template>
  <div class="demo-main">
    <search></search>
    <select-fun></select-fun>
    <content></content>
    <tab-control :titles="tanControlTitle"></tab-control>
  </div>
</template>

<script scope>
import { defineComponent } from 'vue'
import SelectFun from './select/select.vue'
import Search from './search/search.vue'
import Content from './content/content.vue'
import TabControl from './tabControl/tabcontrol.vue'

export default defineComponent({
  name: 'demo-main',
  components: { SelectFun, Search, Content, TabControl },
  setup() {
    const tanControlTitle = [
      {
        title: '工作',
        url: require('@/assets/img/office.png')
      },
      {
        title: '消息',
        url: require('@/assets/img/message.png')
      },
      {
        title: '我的',
        url: require('@/assets/img/user.png')
      }
    ]

    return { tanControlTitle }
  }
})
</script>

<style lang="less" scoped>
.demo-main {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
