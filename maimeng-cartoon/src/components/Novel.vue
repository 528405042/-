<template>
  <div>
    <Header></Header>
    <div class="content-list">
      <div class="content-item">
        <div class="title">古代言情</div>
        <div class="des">山无棱 天地合 才敢与君绝</div>
        <span class="icon"><img src="../common/icon/forword.png"></span>
      </div>
      <div class="content">
        <div class="cover"></div>
        <div class="right">
          <h2 class="name"></h2>
          <div class="author"></div>
          <span class="categoryLabel"></span>
          <div class="introduction"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import Header from './Header'

  export default {
    components: {
      Header
    }
  }
</script>

<style lang="less" scoped>
  .content-list{
    position: relative;
    width: 100%;
    .content-item{
      width: 100%;
      height: 40px;
      display: inline-block;
      padding: 5px;
      border-top: 8px solid #f2f2f2;
      .title{
        position: absolute;
        display:block;
        height: 100%;
        width: 30%;
        padding-left: 10px;
        vertical-align: middle;
        font-size: 20px;
        font-weight: 700;
      }
      .des{
        position: absolute;
        display: block;
        height: 100%;
        width: 50%;
        font-size: 13px;
        top:21px;
        left:27%;
        vertical-align:middle;
        padding-left: 5px;
      }
      .icon{
        position: absolute;
        display: block;
        height: 100%;
        width: 20%;
        left:80%;
        img{
          position: absolute;
          width: 30px;
          height: 30px;
          right: 0;
        }
      }
    }
  }
</style>
