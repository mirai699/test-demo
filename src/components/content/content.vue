<template>
  <div class="content">
    <div class="contentTitle">
      <div class="title">
        <span class="hetitle">岗位</span>
        <img src="@/assets/img/down.png" />
      </div>
      <hr />
      <div class="bottom">
        <div class="bottomTitle">
          <div class="bleft">{{ postTitle.postName }}</div>
          <div class="bright">{{ postTitle.date }}</div>
        </div>
        <div class="bottomContent">
          <div class="left">
            <div class="time">
              <span class="sleft">工作时长</span>
              <span>{{ postTitle.dur }}小时/天</span>
            </div>
            <div class="place">
              <span class="sleft">工作地点</span>
              <span>{{ postTitle.place }}</span>
            </div>
            <div class="contacts">
              <span class="sleft">联系人</span>
              <span>{{ postTitle.contacts }}</span>
            </div>
          </div>
          <div class="right">
            <div class="num">
              <span class="people">人数</span>
              <span>{{ postTitle.num }}</span>
            </div>
            <button>点击了解</button>
          </div>
        </div>
      </div>
    </div>

    <content-items :posts="posts"></content-items>
    <div class="h"></div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import contentItems from './content-items.vue'

export default defineComponent({
  name: 'content',
  components: { contentItems },
  setup() {
    const postTitle = {
      postName: '图书管理员',
      date: '2022-08-12',
      dur: '4',
      place: '第一图书馆',
      contacts: '第一图书馆办公室',
      num: 6
    }
    const posts = [
      {
        postName: '图书馆助理',
        date: '2022-07-10',
        dur: '4',
        place: '第一图书馆',
        contacts: '第一图书馆办公室',
        num: 4
      },
      {
        postName: '图书馆助理',
        date: '2022-07-10',
        dur: '4',
        place: '第一图书馆',
        contacts: '第一图书馆办公室',
        num: 2
      },
      {
        postName: '图书馆助理',
        date: '2022-07-10',
        dur: '4',
        place: '第一图书馆',
        contacts: '第一图书馆办公室',
        num: 2
      },
      {
        postName: '图书馆助理',
        date: '2022-07-10',
        dur: '4',
        place: '第一图书馆',
        contacts: '第一图书馆办公室',
        num: 2
      }
    ]
    return { postTitle, posts }
  }
})
</script>

<style lang="less" scoped>
.content {
  flex: 7;
  display: flex;
  flex-direction: column;

  .contentTitle {
    padding: 20px;
    background-color: #fff;
    height: 170px;
    .title {
      font-size: 26px;
      font-weight: normal;
      margin-bottom: 10px;
      line-height: 35px;
      display: flex;

      .hetitle {
        margin-right: 20px;
      }
    }
    hr {
      width: 80%;
      margin-bottom: 10px;
    }
  }
}
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
.h {
  height: 88px;
}
</style>
