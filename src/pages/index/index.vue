<template>
  <div class="container">

    <!--头部-->
    <div class="shop">
      <!--<img class="background" src="../../assets/images/background.png" alt="">-->
      <div class="shopInfo">
        <img class="shopImg" src="../../assets/images/shopimg.jpeg" alt="">
        <div class="shopDes">
          <i class="icon-caidanlanwode"></i>
          <p>配送约30分钟</p>
          <span>公告：本店已加盟美团外卖，美团订单优先配送！</span>
          <ul class="Discount">
            <li class="reduce">30减7</li>
            <li class="reduce">40减10</li>
            <li class="reduce">首单减10</li>
          </ul>
        </div>
      </div>
    </div>

    <!--导航-->
    <div class="bottomNav">
      <ul>
        <li><a>菜单</a></li>
        <li><a>评论</a></li>
        <li><a>商家</a></li>
        <li><a>我的</a></li>
      </ul>
    </div>

    <!--内容-->
    <div class="content">
      <div class="series">
        <ul class="seriesList">
          <li class="list">热销榜啦啦啦啦啦</li>
          <li class="list">披萨系列</li>
          <li class="list">意面系列</li>
          <li class="list">中餐系列</li>
          <li class="list">小吃系列</li>
          <li class="list">我爱饭米粒</li>
          <li class="list">热饮系列</li>
          <li class="list">鲜榨果汁系列</li>
          <li class="list">单人精品套餐</li>
          <li class="list">特色菜品</li>
          <li class="list">特色菜品</li>
          <li class="list">特色菜品</li>
          <li class="list">特色菜品</li>
        </ul>
      </div>
      <div class="menu"></div>
    </div>



    <!--底部购物车导航-->
    <div class="shopCar">
      <div class="car"><i class="icon-caidanlangouwuche"></i></div>
      <div class="totalPrice">
        <p>￥0</p>
        <p> | </p>
        <p>另需配送费￥4元</p>
      </div>
      <div class="delivery"><p>￥20元起送</p></div>
    </div>

  </div>
</template>

<script>

  export default {
    data () {
      return {
      }
    },

    components: {
    },

    methods: {
    },

    created () {

    }
  }
</script>

<style scoped>
  .container{
    width: 100%;
    height: 592px;
    position: relative;
  }
  .shop{
    width: 100%;
    height: 100px;
    background-color: black;
    position: fixed;
    top: 0;
  }
  .shop .background{
    width: 100%;
    height: 100px;
  }
  .shopInfo {}
  .shopImg{
    width: 60px;
    height: 60px;
    position: absolute;
    top: 20px;
    left: 20px;
    float: left;
  }
  .shopDes{
    position: absolute;
    top: 20px;
    left: 100px;
    height: 60px;
    width: 260px;
  }
  .shopDes i{
    color: orange;
    display: inline-block;
    float: left;
    margin-right: 5px;
  }
  .shopDes p{
    color: #fff;
    font-size: 12px;
    margin-bottom: 8px;
  }
  .shopDes span{
    color: #fff;
    font-size: 12px;
    float: left;
    margin-bottom: 2px;
  }
  .Discount{}
  .reduce{
    color: #fff;
    background-color: red;
    font-size: 12px;
    display: inline-block;
    margin-right: 10px;
    padding: 2px;
  }
  .content{
    width: 100%;
    height: 450px;
  }
  .series{
    width: 19.7%;
    height: 450px;
    float: left;
    background-color: #f6f9f9;
    border-right: 1px solid #000;
  }
  .menu{
    width: 80%;
    float: right;
    height: 450px;
    background-color: blue;
  }
  .seriesList{
    margin: 0;
    padding: 0;
    position: absolute;
    top: 140px;
  }
  .list{
    width: 100%;
    height: 50px;
    line-height: 50px;
    font-size: 14px;
    text-align: center;
    word-wrap:break-word;
    word-break:normal;
    overflow: hidden;
    border-bottom: 1px solid #ddd;
  }


  .bottomNav{
    width: 100%;
    height: 40px;
    background-color: #fff;
    position: fixed;
    top: 100px;
  }
  ul{
    margin: 0;
    padding: 0;
  }
  .bottomNav li{
    margin: 0;
    padding: 0;
    list-style: none;
    text-decoration: none;
    display: inline-block;
    width: 94px;
    height: 40px;
    text-align: center;
    border-bottom: 1px solid #ccc;
    border-top: 1px solid #ccc;
    line-height: 40px;
  }
  .bottomNav a{
    font-size: 15px;
  }
  .shopCar{
    width: 100%;
    height: 50px;
    background-color: #141c26;
    position: fixed;
    bottom: 0;
  }
  .shopCar .car{
    width: 50px;
    height: 50px;
    background-color: #2a343c;
    border-radius: 50%;
    position: absolute;
    bottom: 5px;
    left: 10px;
    border: 5px solid #141c26;
  }
  .shopCar .car i {
    font-size: 30px;
    color: #7e848a;
    font-weight: 700;
    position: absolute;
    left: 10px;
    bottom: 8px;
  }
  .delivery{
    float: right;
    width: 100px;
    height: 50px;
    background-color: #2a323a;
  }
  .delivery p {
    color: #7e848a;
    line-height: 50px;
    font-size: 14px;
    text-align: center;
  }
  .totalPrice{
    float: left;
    color: #70777d;
    position: absolute;
    left: 70px;
  }
  .totalPrice p{
    font-size: 14px;
    display: inline-block;
    line-height: 50px;
    margin-right: 5px;
  }
</style>
