<template>
  <div id="app">
    <header>
      <!-- <div class="left"> -->
      <ul class="clearfix">
        <li><img src="./assets/images/icon_home_active@3x.png" alt="">图美丽商城</li>
        <li>hello,欢迎来到图美丽</li>
        <li><a href="javascript:;">请登录</a> </li>
        <li><a href="javascript:;">免费注册</a> </li>
        <li><img src="./assets/images/icon_cart_active@3x.png" alt=""><a href="javascript:;">我的购物车</a></li>
      </ul>
    </header>
    <router-view/>
    <footer>
      <div class="title" v-if="isShow">
        <img src="./assets/images/icon_category_active@3x.png" alt="">
        <span>图美丽 | 智能版</span>
        </div>
      <div class="quality">
        <ul class="clearfix">
          <li>
            <div class="iconBox"></div>
            <div class="textBox">
              <h3>品质保障</h3>
              <p>品质保障</p>
            </div>
          </li>
          <li>
            <div class="iconBox"></div>
            <div class="textBox">
              <h3>品质保障</h3>
              <p>品质保障</p>
            </div>
          </li>
          <li>
            <div class="iconBox"></div>
            <div class="textBox">
              <h3>品质保障</h3>
              <p>品质保障</p>
            </div>
          </li>
          <li>
            <div class="iconBox"></div>
            <div class="textBox">
              <h3>品质保障</h3>
              <p>品质保障</p>
            </div>
          </li>
          <li>
            <div class="iconBox"></div>
            <div class="textBox">
              <h3>品质保障</h3>
              <p>品质保障</p>
            </div>
          </li>
        </ul>
      </div>
      <div class="aboutUs">
        <a href="javascript:;">增值电信业务经营许可证：66666666</a>
        <a href="javascript:;">增值电信业务经营许可证：66666666</a>
        <a href="javascript:;">12318举报</a>
        <a href="javascript:;">出版物网络交易平台服务经营备案证： 新出发浙备字第001号</a>
        <div>
          <a href="javascript:;">互联网违法和不良信息举报电话：0571-81683755 blxxjb@alibaba-inc.com</a>
          <a href="javascript:;"> 互联网药品信息服务资质证书编号：6666666666</a>
          <a>浙公网安备 33010002000120号</a>
        </div>
        <p>© 2003-2018 TMALL.COM 版权所有</p>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      isShow: false
    }
  },
  mounted () {
    // console.log(this.$route.path)
    if (this.$route.path === '/') {
      this.isShow = true
    }
  }
}
</script>

<style lang="scss" scoped>
*{
margin:0;
padding:0;
box-sizing: border-box;
list-style: none;
}
header{
  background:#f2f2f2;
  width:100%;
 ul{
     height:50px;
     padding:10px 80px;
     width:1200px;
    li{
      float:left;
       line-height: 30px;
      font-size: 16px;
      color:#666;;
      margin:0 25px;
      a{
        color:inherit;
      }
      img{
        width:20px;
        height:20px;
        float: left;
        margin-top:4px;
      }
    }
    li:last-child{
      margin-left:350px;
    }
  }
  }
footer{
  .title{
    text-align: center;
    border:1px solid #ccc;
    padding:15px 0;
    img{
      width:20px;
      height:20px;
      vertical-align: bottom;
    }
  }
  .quality{
    width:1380px;
    padding:35px 100px;
    border-bottom:1px solid #ccc;
    ul{
      li{
        float:left;
        width:20%;
        .iconBox{
          width:55px;
          height:50px;
          background:url(./assets/images/icons.png) no-repeat -252px -2px;
          float:left;
        }
        .textBox{
          float:left;
          h3{
            margin:5px 0;
          }
        }
      }
      li:nth-child(2){
        .iconBox{
           background:url(./assets/images/icons.png) no-repeat -252px -54px;
        }
      }
      li:nth-child(3){
        .iconBox{
           background:url(./assets/images/icons.png) no-repeat -252px -106px;
        }
      }
      li:nth-child(4){
        .iconBox{
           background:url(./assets/images/icons.png) no-repeat -252px -157px;
        }
      }
      li:nth-child(5){
        .iconBox{
           background:url(./assets/images/icons.png) no-repeat -253px -208px;
        }
      }
    }
  }
  .aboutUs{
    background:#000;
    padding:20px 50px;
    text-align: center;
    a{
      color:#ccc;
      display:inline-block;
      padding:0 20px;
    }
  }
}
/*清除浮动*/
.clearfix:after {
    visibility: hidden;
    clear: both;
    display: block;
    content: ".";
    height: 0;
    line-height: 0;
}

.clearfix {
    *zoom: 1;
}
</style>
