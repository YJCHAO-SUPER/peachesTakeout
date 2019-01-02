<template>
  <div class="container">

    <!--头部-->
    <div class="shop">
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
          <li class="list" v-for="(typeItem,t) in type" :key="t" @click="anchorPoint(t)">{{ typeItem.name }}</li>
        </ul>
      </div>
      <scroll-view class="menu" id="menu" scroll-view="scroll" scroll-y="true">
        <div class="dishList" id="d1" v-for="(item, index) in foodMenu" :key="index">
          <span class="currentSeries">{{ item.name }}</span>
          <ul class="dishSeries">
            <li class="dishName" v-for="(dish,k) in item.foodList" :key="k">
              <img :src="dish.img" alt="">
              <div class="dishContent">
                  <span class="dishTitle">{{ dish.food_name }}</span>
                  <p class="assess">月售 {{ dish.sale_count }} &nbsp;&nbsp;赞 {{ dish.like_count }} </p>
                  <span class="dishPrise">￥{{ dish.price }}</span>
              </div>
              <span class="add" @click="add(dish.id)">+</span>
            </li>
          </ul>
        </div>
      </scroll-view>
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
        foodMenu: [
            {
              id: 1,
              name: "热销榜",
              foodList: [
                {
                  id: 1,
                  img: "http://cp1.douguo.net/upload/caiku/0/8/b/yuan_0842a0a8ab653ea955b4d3a98cf06b3b.jpeg",
                  food_name: "桃酱蛋糕",
                  sale_count: 123,
                  like_count: 33,
                  price: 145
                },
                {
                  id: 5,
                  img: "http://cp1.douguo.net/upload/caiku/0/8/b/yuan_0842a0a8ab653ea955b4d3a98cf06b3b.jpeg",
                  food_name: "桃酱sadasd蛋糕",
                  sale_count: 1223,
                  like_count: 333,
                  price: 1345
                },
                {
                  id: 2,
                  img: "https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=2800752024,3815278738&fm=26&gp=0.jpg",
                  food_name: "红酒桃子蛋挞",
                  sale_count: 199,
                  like_count: 178,
                  price: 112
                },
                {
                  id: 3,
                  img: "https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=3507601575,100000529&fm=26&gp=0.jpg",
                  food_name: "桃子汽水",
                  sale_count: 14,
                  like_count: 11,
                  price: 5
                },
              ]
            },
            {
              id: 2,
              name: "披萨系列",
              foodList: [
                {
                  id: 1,
                  img: "https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=608559660,4001250914&fm=26&gp=0.jpg",
                  food_name: "桃子披萨",
                  sale_count: 100,
                  like_count: 15,
                  price: 100
                },
                {
                  id: 1,
                  img: "https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=608559660,4001250914&fm=26&gp=0.jpg",
                  food_name: "桃子披萨",
                  sale_count: 100,
                  like_count: 15,
                  price: 100
                },{
                  id: 1,
                  img: "https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=608559660,4001250914&fm=26&gp=0.jpg",
                  food_name: "桃子披萨",
                  sale_count: 100,
                  like_count: 15,
                  price: 100
                },{
                  id: 1,
                  img: "https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=608559660,4001250914&fm=26&gp=0.jpg",
                  food_name: "桃子披萨",
                  sale_count: 100,
                  like_count: 15,
                  price: 100
                },{
                  id: 1,
                  img: "https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=608559660,4001250914&fm=26&gp=0.jpg",
                  food_name: "桃子披萨",
                  sale_count: 100,
                  like_count: 15,
                  price: 100
                },{
                  id: 1,
                  img: "https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=608559660,4001250914&fm=26&gp=0.jpg",
                  food_name: "桃子披萨",
                  sale_count: 100,
                  like_count: 15,
                  price: 100
                },{
                  id: 1,
                  img: "https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=608559660,4001250914&fm=26&gp=0.jpg",
                  food_name: "桃子披萨",
                  sale_count: 100,
                  like_count: 15,
                  price: 100
                },{
                  id: 1,
                  img: "https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=608559660,4001250914&fm=26&gp=0.jpg",
                  food_name: "桃子披萨",
                  sale_count: 100,
                  like_count: 15,
                  price: 100
                },
              ]
            },
          ],
        type:[
          {
            id:1,
            name:"热销榜"
          },
          {
            id:2,
            name:"披萨系列"
          },
          {
            id:3,
            name:"意面系列"
          },
          {
            id:4,
            name:"中餐系列"
          },
          {
            id:5,
            name:"小吃系列"
          },
          {
            id:6,
            name:"我爱饭米粒"
          },
          {
            id:7,
            name:"热饮系列"
          },
          {
            id:8,
            name:"鲜榨果汁系列"
          },{
            id:9,
            name:"单人精品套餐"
          }
        ],
        scroll: 0
      }
    },

    components: {
    },

    methods: {

      anchorPoint(index){
        let goods = 0
        //标题高度
        let title = index*8;
        //系列高度
        let seriesHeight = index*30;
        for (let i=0;i<index;i++){
          //商品高度
           goods  = goods+(47*this.foodMenu[i].foodList.length)
        }
        this.scroll= title+goods+seriesHeight;

      },
      add(goodsId){
        console.log(goodsId)
      }

    },

    created () {

    }
  }

  /*锚点*/



</script>

<style scoped>
  .container{
    width: 100%;
    height: 592px;
    position: relative;
  }
  .shop{
    width: 100%;
    height: 17%;
    background-color: black;
    position: fixed;
    top: 0;
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
  .bottomNav{
    width: 100%;
    height: 7%;
    background-color: #fff;
    position: fixed;
    top: 17%;
    overflow: hidden;
    border-bottom: 1px solid #ddd;
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
  .content{
    width: 100%;
    height: 68%;
    overflow: hidden;
    position: fixed;
    top: 24%;
  }
  .series{
    width: 20%;
    float: left;
    height: 100%;
    background-color: #f6f9f9;
  }
  .seriesList{
    height: 100%;
    overflow-x: hidden;
    overflow-y: scroll;
    margin: 0;
    padding: 0;
  }
  .seriesList::-webkit-scrollbar {
    display: none;
  }
  .list{
    width: 100%;
    line-height: 25px;
    padding: 12.5px 0;
    font-size: 14px;
    text-align: center;
    word-wrap:break-word;
    word-break:normal;
    overflow: hidden;
  }
  .menu{
    width: 80%;
    float: right;
    height: 100%;
    overflow-x: hidden;
    overflow-y: auto;
  }
  .dishList{
    width: 100%;
    overflow-x: hidden;
    overflow-y: scroll;
    margin-bottom: 30px;
  }
  .dishList::-webkit-scrollbar {
    display: none;
  }
  .currentSeries{
    font-size: 15px;
    width: 100%;
    display: block;
    margin: 15px 15px;
  }
  .dishSeries{
    height: 100%;
    overflow-x: hidden;
    overflow-y: scroll;
    margin: 0;
    padding: 0;
  }
  .dishName{
    width: 100%;
    height: 75px;
    font-size: 14px;
    word-wrap:break-word;
    word-break:normal;
    overflow: hidden;
    position: relative;
    margin-bottom: 15px;
  }
  .dishName img{
    width: 25%;
    height: 100%;
    margin: 0 15px;
    float: left;
  }
  .dishContent{
    height: 100%;
    float: left;
  }
  .dishTitle{
    font-size: 16px;
    font-weight: 800;
  }
  .assess{
    font-size: 12px;
    width: 100%;
    height: 10%;
    padding: 3px 0;
  }
  .dishPrise{
    color: red;
    font-size: 16px;
    font-weight: 600;
    position: absolute;
    bottom: 0;
  }
  .add{
    float: right;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background-color: #fed360;
    text-align: center;
    line-height: 20px;
    color: black;
    font-weight: 800;
    position: absolute;
    bottom: 0;
    right: 10px;
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
