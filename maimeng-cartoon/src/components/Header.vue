<template>
  <div class="header">
    <div class="header-content">
      <div class="header-box">
        <div class="title">麦萌小说</div>
        <form action="" class="header_form">
          <a href="#" class="icon_logo"><img src="../common/icon/search.png"></a>
          <input type="search" placeholder="猫生赢家/路从今夜白"/>
        </form>
        <div>
          <div class="bell"><img src="../common/icon/bell.png"></div>
          <div class="login">登录</div>
        </div>
        <div class="btn_to">
          <span class="recommend">推荐</span>
          <span class="category">类别</span>
        </div>
      </div>
    </div>
    <div class="header_banner">
      <ul class="clearfix">
        <li>
          <img src="http://pic3.maimengjun.com/cf0004a34f3db061774454e120fa6d30.jpg">
        </li>
      </ul>
      <!--<ul>-->
      <!--v-for="item in img2.data"-->
      <!--<img :src="item.images">-->
      <!--<li class="dots"></li>-->
      <!--</ul>-->
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      img2: {
        type: Object
      }
    }
  }
</script>

<style lang="less" scoped>
  .header-content {
    display: flex;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 60px;
    font-size: 0;
    z-index: 1;
    .header-box {
      position: relative;
      margin: 0 auto;
      width: 100%;
      height: 60px;
      max-width: 640px;
      min-width: 300px;
      color: #fff;
      background: #4285f4;
      display: flex;
      .title {
        flex: 0 0 80px;
        position: absolute;
        top: 5px;
        left: 5px;
        display: inline-block;
        width: 80px;
        font-size: 20px;
        border-radius: 20px;
      }
      .icon_logo {
        position: absolute;
        left: 15px;
        top: 15px;
        width: 30px;
        height: 30px;
        z-index: 4;
        img {
          width: 30px;
          height: 30px;
        }
      }
      .header_form {
        flex: 1;
        left: 80px;
        right: 30px;
        position: absolute;
        padding: 0 10px;
        display: inline-block;
        /*width: 250px;*/
        height: 60px;
        /*box-sizing: border-box;*/
        input {
          position: absolute;
          top: 15px;
          padding: 0 10px 0 40px;
          width: 83%;
          height: 30px;
          border-radius: 20px;
          border: none;
          font-size: 14px;
          z-index: 3;
        }
      }
      .bell {
        position: absolute;
        right: 0px;
        top: 0px;
        width: 30px;
        height: 30px;
        display: block;
        line-height: 40px;
        z-index: 4;
        img {
          width: 20px;
          height: 20px;
        }
      }
      .login {
        position: absolute;
        right: 25px;
        top: 12px;
        width: 30px;
        height: 30px;
        font-size: 15px;
        color: #fff;
        display: block;
        line-height: 40px;
        z-index: 4;
      }
    }
  }

  .header_banner {
    position: relative;
    width: 100%;
    height: 200px;
    /*overflow: hidden;*/
    border: 1px solid #ccc;
    list-style: none;
    z-index: -1;
    ul:first-child {
      width: 500%;
      /*transform: translateX(-10%);*/
      li {
        float: left;
        width: 5%;
        img {
          width: 100%;
          display: block;
        }
      }
    }
  }
</style>
