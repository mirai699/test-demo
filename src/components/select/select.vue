<template>
  <div class="nav">
    <div class="item" v-for="(item, index) in navdata" :key="index" @click="handleClick(index)">
      <img :src="item.url" />
      <span>{{ item.title }}</span>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'select-fun',

  setup() {
    const navdata = [
      {
        title: '时间',
        url: require('@/assets/img/time.png')
      },
      {
        title: '地点',
        url: require('@/assets/img/position.png')
      },
      {
        title: '岗位',
        url: require('@/assets/img/post.png')
      }
    ]

    const handleClick = (index) => {
      console.log('点击了' + index)
    }

    return { navdata, handleClick }
  }
})
</script>

<style lang="less" scoped>
.nav {
  margin-top: 90px;
  flex: 2;
  height: 100%;
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin-bottom: 10px;
  background-color: white;
  padding: 20px;
  .item {
    display: flex;
    flex-direction: column;
    text-align: center;
    img {
      height: 90px;
      width: 90px;
    }
    span {
      font-size: 20px;
      font-weight: 500;
    }
  }
}
</style>
