<template>
  <div class="search">
    <span class="searchs">
      <input type="search" placeholder="搜索地点、时间" />
    </span>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'search',
  setup() {
    return {}
  }
})
</script>

<style lang="less" scoped>
.search {
  width: 100%;
  height: 90px;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background-color: rgb(19, 65, 102);
  .searchs {
    input {
      height: 50%;
      width: 80%;
      margin-left: 10%;
      border-radius: 23px;
      border: none;
      margin-top: 20px;
      text-indent: 50px;
      background: url(@/assets/img/search.png) no-repeat;
      background-color: #fff;
      background-position: 18px 11px;
    }
    input::-webkit-input-placeholder {
      color: black;
      font-size: 16px;
    }
  }
}
</style>
