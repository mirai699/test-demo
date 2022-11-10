<template>
  <div class="content-items">
    <template v-for="(item, index) in posts" :key="index">
      <div class="contentPost">
        <div class="bottom">
          <div class="bottomTitle">
            <div class="bleft">{{ item.postName }}</div>
            <div class="bright">{{ item.date }}</div>
          </div>
          <div class="bottomContent">
            <div class="left">
              <div class="time">
                <span class="sleft">工作时长</span>
                <span>{{ item.dur }}小时/天</span>
              </div>
              <div class="place">
                <span class="sleft">工作地点</span>
                <span>{{ item.place }}</span>
              </div>
              <div class="contacts">
                <span class="sleft">联系人</span>
                <span>{{ item.contacts }}</span>
              </div>
            </div>
            <div class="right">
              <div class="num">
                <span class="people">人数</span>
                <span>{{ item.num }}</span>
              </div>
              <button @click="handleKnow">点击了解</button>
            </div>
          </div>
        </div>
      </div>
    </template>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'content-items',
  props: {
    posts: {
      type: Array,
      default() {
        return []
      }
    }
  },
  setup() {
    const handleKnow = () => {
      console.log('点击了解')
    }
    return { handleKnow }
  }
})
</script>

<style lang="less" scoped>
.bottom {
  .bottomTitle {
    display: flex;
    justify-content: space-between;
    font-size: 20px;
    font-weight: 800;

    .bright {
      color: rgb(6, 93, 151);
    }
  }

  .bottomContent {
    display: flex;
    justify-content: space-between;
    color: rgb(177, 174, 174);
    font-size: 15px;
    font-weight: 500;

    .left {
      .time,
      .place,
      .contacts {
        margin-top: 10px;

        .sleft {
          margin-right: 20px;
          display: inline-block;
          width: 60px;
        }
      }
    }

    .right {
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      .people {
        display: inline-block;
        margin-top: 10px;
        margin-right: 10px;
      }

      button {
        background-color: rgb(6, 93, 151);
        color: #fff;
        width: 90px;
        border-radius: 5px;
        height: 30px;
        border: none;
      }
    }
  }
}
.contentPost {
  margin-top: 10px;
  padding: 20px;
  background-color: #fff;
}
</style>
