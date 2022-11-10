<template>
  <div class="tabcontrol">
    <div class="tab-control">
      <div v-for="(item, index) in titles" :key="index" class="tab-control-item">
        <img :src="item.url" />
        <span>{{ item.title }}</span>
      </div>
    </div>
  </div>
</template>

<script scope>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'tabcontrol',
  props: {
    titles: {
      type: Array,
      default() {
        return []
      }
    }
  },
  setup() {
    return {}
  }
})
</script>

<style lang="less" scoped>
.tab-control {
  display: flex;
  text-align: center;
  font-size: 13px;
  font-weight: 500;
  background-color: #fff;
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  border-top: 1px solid rgb(218, 218, 218);
  padding: 10px 0;

  .tab-control-item {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;

    span {
      padding: 5px;
    }
    img {
      width: 40px;
      height: 40px;
    }
  }
  .active {
    color: var(--color-high-text);

    span {
      border-bottom: 3px solid var(--color-tint);
    }
  }
}
</style>
