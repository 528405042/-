<template>
  <div id="app">
    <div class="tab-box">
      <div class="tab-item">
        <router-link to="/novel">
          <div class="box">
            <div class="icon"><img src="./common/icon/book.png"></div>
            <div class="click-name">小说</div>
          </div>
        </router-link>
      </div>
      <div class="tab-item">
        <router-link to="/comic">
          <div class="box">
            <div class="icon"><img src="./common/icon/comic.png"></div>
            <div class="click-name">漫画</div>
          </div>
        </router-link>
      </div>
      <div class="tab-item">
        <router-link to="/community">
          <div class="box">
            <div class="icon"><img src="./common/icon/community.png"></div>
            <div class="click-name">社区</div>
          </div>
        </router-link>
      </div>
      <div class="tab-item">
        <router-link to="/bookbase">
          <div class="box">
            <div class="icon"><img src="./common/icon/books.png"></div>
            <div class="click-name">书架</div>
          </div>
        </router-link>
      </div>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data () {
      return {
        img2: {}
      }
    },
    created () {
      let self = this
      this.$axios.get('/api/img2')
        .then((res) => {
          console.log(res)
          res = res.data
          if (res.error === 0) {
            self.img2 = res.data
          }
        })
        .catch((error) => {
          alert(error)
        })
    }
  }
</script>

<style lang="less">
  #app {
    .tab-box {
      display: flex;
      position: fixed;
      bottom: 0;
      height: 60px;
      width: 100%;
      border-top: 2px solid rgba(7, 17, 27, 0.1);
      .tab-item {
        flex: 1;
        text-align: center;
        .box{
          height: 100%;
          .icon img{
            padding: 5px;
            width: 30px;
            height: 30px;
            &.active{
              background-color: #fe5567;
            }
          }
          .click-name{
            font-size: 14px;
            height: 20px;
          }
        }
        & > a {
          display: block;
          color: rgb(77, 85, 93);
        }
      }
    }
  }
</style>
