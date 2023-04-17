<template>
  <div class="solution">
    <div class="pc">
      <div class="selection selection-1">
        <app-header v-if="show"></app-header>
        <transition name="bounce" enter-active-class="bounceInDown" leave-active-class="bounceOutDown">
          <div v-if="show" class="left_bg">
            <div class="cont">
              <transition name="fade" enter-active-class="fadeInUp" leave-active-class="fadeOutUp">
                <h1 v-if="show_02">什么是物联网智能<br/>净水器一站式解决方案？</h1>
              </transition>
              <transition name="fade" enter-active-class="fadeInUp" leave-active-class="fadeOutUp">
                <p v-if="show_02">传统净水器+物联网电脑板+GPRS连接互联网+<br/>手机客户端+云计算平台+运营管理平台</p>
              </transition>
            </div>
          </div>
        </transition>
        <transition name="bounce" enter-active-class="bounceInUp" leave-active-class="bounceOutUp">
          <div v-if="show" class="right_bg">
            <div class="cont">
              <transition name="fade" enter-active-class="fadeInUp" leave-active-class="fadeInUp">
                <h2 v-if="show_02">物联网+智能共享无压力消费模式</h2>
              </transition>
              <transition name="fade" enter-active-class="fadeInUp" leave-active-class="fadeInUp">
                <p v-if="show_02"> 无需购买净水器！仅需¥180元初装费<br/>
                    价值¥5680的蓝密码RO反渗透净水机免费用上一辈子！<br/>
                    1.打开手机，连接设备实时监控<br/>
                    2.产品更新，立即免费升级置换<br/>
                    3.滤芯到期，终生免费更换<br/>
                    4.设备损坏，免费维护换新
                </p>
              </transition>
            </div>
          </div>
        </transition>
      </div>
      <div class="selection selection-2">
        <div class="con">
          <div class="discr-con">
            <h2 class="title">套餐类型</h2>
          </div>
          <div class="cont">
            <div class="list_div">
              <div class="list_div_con">
                <h1>A</h1>
                <h4>不限量豪饮套餐</h4>
                <p>（多口之家、门店、公司的不二之选）</p>
              </div>
            </div>
            <div class="list_div">
              <div class="list_div_con">
                <h1>B</h1>
                <h4>不限时超值套餐</h4>
                <p>¥980=3500升=¥0.28元/升<br/>
                  ¥1280=5000升=¥0.25元/升<br/>
                  ¥1680=8000升=¥0.21元/升<br/>
                  Ps：仅比社区净水器贵1分钱<br/>
                  （每人饮水量约1.2-2升/日，<br/>
                  三口之家食用水约10升/日）
                </p>
              </div>
            </div>
          </div>
          <img src="../assets/37.png" alt="">
        </div>
        <app-footer></app-footer>
      </div>
    </div>
    <div class="mob">
      <div class="selection selection-1">
        <app-header></app-header>
          <div class="cont">
            <h1>什么是物联网智能<br/>净水器一站式解决方案？</h1>
            <p class="discr">传统净水器+物联网电脑板+<br/>GPRS连接互联网+手机客户端+<br/>云计算平台+运营管理平台</p>
            <h2>物联网+智能共享无压力消费模式</h2>
            <p> 无需购买净水器！仅需¥180元初装费<br/>
              价值¥5680的蓝密码RO反渗透净水机免费用上一辈子！<br/>
              1.打开手机，连接设备实时监控<br/>
              2.产品更新，立即免费升级置换<br/>
              3.滤芯到期，终生免费更换<br/>
              4.设备损坏，免费维护换新
            </p>
            <button class="down-btn" @click="slideDown">
              <i class="icon-Group-47"></i>
            </button>
        </div>
      </div>
      <div class="selection selection-2">
        <div class="con">
          <div class="discr-con">
            <h2 class="title">套餐类型</h2>
          </div>
          <div class="cont">
            <div class="cont_">
              <div class="list_div">
                <div class="list_div_con">
                  <h1>A</h1>
                  <h4>不限量豪饮套餐</h4>
                  <p>（多口之家、门店、公司的不二之选）</p>
                </div>
              </div>
              <div class="list_div">
                <div class="list_div_con">
                  <h1>B</h1>
                  <h4>不限时超值套餐</h4>
                  <p>¥980=3500升=¥0.28元/升<br/>
                    ¥1280=5000升=¥0.25元/升<br/>
                    ¥1680=8000升=¥0.21元/升
                  </p>
                  <p class="ps">Ps：仅比社区净水器贵1分钱<br/>
                    （每人饮水量约1.2-2升/日，<br/>
                    三口之家食用水约10升/日）</p>
                </div>
              </div>          
            </div>
          </div>
          <img src="../assets/014.svg" alt="">
        </div>
      </div>
      <app-footer></app-footer>
    </div>
  </div>
</template>

<script>
import Header from './Header'
import Footer from './Footer'
export default {
  name: 'Solution',
  data () {
    return {
      show: false,
      show_02: false
    }
  },
  created() {
    let _this = this;
    setTimeout(() => {
      _this.show = true;
    }, 10);
    setTimeout(() => {
      _this.show_02 = true;
    }, 800);
  },
  methods: {
    slideDown() {
      let downHeight = document.documentElement.clientHeight;
      window.scrollTo(0, downHeight);
      this.slideShow = true;
    }
  },
  mounted() {
    $('.selection-2 .list_div').on('click', function() {
      if($(this).hasClass('list_div_sel')) {
        $(this).removeClass('list_div_sel');
      } else {
        $(this).addClass('list_div_sel').siblings().removeClass('list_div_sel');
      }
    });
  },
  components: {
    'app-header': Header,
    'app-footer': Footer
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /*selection-1*/
  .selection-1 {
    width: 100%;
    height: 100vh;
    overflow: hidden;
  }

  .selection-1 .left_bg {
    display: flex;
    align-items: center;
    justify-content: center;
    float: left;
    width: 50%;
    height: 100%;
    background: url('../assets/35.jpg') center center no-repeat;
    background-size: 100% 100%;
  }
  .selection-1 .right_bg {
    display: flex;
    align-items: center;
    justify-content: center;
    float: left;
    width: 50%;
    height: 100%;
    background: url('../assets/36.jpg') center center no-repeat;
    background-size: 100% 100%;
  }
  .selection-1 .left_bg .cont {
    width: 80%;
  }
  .selection-1 .right_bg .cont {
    width: 55%;
    margin: 0;
  }

  .selection-1 .left_bg h1 {
    margin-bottom: 5.83vh;
    color: #FFFFFF;
    text-align: center;
    font-size: 3.39vw;
    font-weight: 600;
  }
  .selection-1 .left_bg p {
    color: #58B2FF;
    text-align: center;
    line-height: 2.3vw;
    font-size: 1.4vw;
  }

  .selection-1 .right_bg h2 {
    margin-bottom: 3.33vh;
    color: #58B2FF;
    font-size: 1.82vw;
  }
  .selection-1 .right_bg p {
    color: #FFFFFF;
    line-height: 1.98vw;
    font-size: 1.04vw;
  }
  
  /*selection-2*/
  .selection-2 {

  }
  .con {
    height: 78.7vh;
  }
  .selection-2 .discr-con {
    padding-top: 8.98vh;
  }
  .selection-2 .title {
    color: #000;
  }
  .selection-2 .cont {
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    width: 100%;
    margin-top: 2.78vh;
    margin-bottom: 6.76vh;
  }
  .selection-2 .list_div {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 21.35vw;
    height: 21.35vw;
    margin: 0 9.06vw;
    overflow: hidden;
    border-radius: 50%;
    background: #FFFFFF;
    box-shadow: 0 21px 44px 0 rgba(0,0,0,0.12);
    cursor: pointer;
    -webkit-transition: all 0.8s;
    transition: all 0.8s;
  }
  
  .selection-2 .con img {
    display: block;
    width: 36.41vw;
    margin: 0 auto;
  }
  .selection-2 .list_div h1 {
    height: 7.2vw;
    line-height: 5.2vw;
    font-size: 6.51vw;
    font-weight: 600;
  }
  .selection-2 .list_div h4 {
    font-size: 1.82vw;
  }
  .selection-2 .list_div p {
    display: none;
    font-size: 1.82vw;
  }
  
  
  @media screen and (max-width: 750px) {
    .selection-1 {
      position: relative;
      width: 100%;
      height: 100vh;
      overflow: hidden;
      background: url('../assets/013.jpg') center center no-repeat;
      background-size: cover;
    }
    .selection-1 .cont {
      height: 76.74vh;
      padding-top: 23.26vh;
    }
    .selection-1 h1 {
      margin-bottom: 1.95vh;
      color: #fff;
      text-align: center;
      line-height: 8.3vw;
      font-size: 7.47vw;
      font-weight: 600;
    }
    .selection-1 .discr {
      position: relative;
      margin-bottom: 12.29vh;
      color: #58B2FF;
      text-align: center;
      font-size: 4.8vw;
    }
    .selection-1 p {
      font-size: 3.2vw;
      color: #58B2FF;
      text-align: center;
      line-height: 5.33vw;
    }
    .selection-1 h2 {
      margin-bottom: 3.4vh;
      text-align: center;
      color: #FFFFFF;
      font-size: 4.8vw;
    }
    .selection-1 .discr:after {
      content: '';
      position: absolute;
      left: 0;
      bottom: -5.85vh;
      width: 100%;
      height: 0.45vh;
      font-size: 2vw;
      background: url('../assets/3.svg') center center no-repeat;
      background-size: auto 100%;
    }

    .selection-2  {
      height: 123.74vh;
    }
    .selection-2 .discr-con {
      padding-top: 7.8vh;
    }
    .selection-2 .cont {
      width: 100%;
      margin-top: 2.78vh;
      margin-bottom: 0;
    }
    .selection-2 .con {
      height: 100%;
    }
    .selection-2 .cont_ {

    }
    .selection-2 .list_div {
      width: 60.8vw;
      height: 60.8vw;
      margin: 0 auto 3.9vh;
    }
    .selection-2 .list_div h1 {
      height: 23.2vw;
      line-height: 21.33vw;
      font-size: 26.67vw;
    }
    .selection-2 .list_div h4 {
      font-size: 4.8vw;
      line-height: 5.33vw;
    }

    .selection-2 .list_div_sel {
      color: #fff;
      background: #58B2FF;
      -webkit-transition: all 0.8s;
      transition: all 0.8s;
    }
    .selection-2 .list_div_sel h1 {
      height: 11vw;
      font-size: 11.2vw;
      line-height: 8.4vw;
    }
    .selection-2 .list_div_sel h4 {
      margin-bottom: 1.4vh;
      font-size: 4.8vw;
      line-height: 5.33vw;
    }
    .selection-2 .list_div_sel p {
      display: block;
      font-size: 3.2vw;
      line-height: 5.33vw;
    }
    .selection-2 .list_div_sel .ps {
      font-size: 2.4vw;
    }

    /*.selection-2 .list_div:hover h1 {
      height: 11vw;
      font-size: 11.2vw;
      line-height: 8.4vw;
    }
    .selection-2 .list_div:hover h4 {
      font-size: 4.8vw;
      line-height: 5.33vw;
    }
    .selection-2 .list_div:hover p {
      font-size: 3.2vw;
      line-height: 5.33vw;
    }
    .selection-2 .list_div:hover .ps {
      font-size: 2.4vw;
    }*/

    .selection-2 .con img {
      width: 60vw;
    }
  }
  @media screen and (min-width: 751px) {
    .selection-2 .list_div:hover {
      color: #fff;
      background: #58B2FF;
      -webkit-transition: all 0.8s;
      transition: all 0.8s;
    }
    .selection-2 .list_div:hover h1 {
      height: 3.5vw;
      line-height: 3.2vw;
      font-size: 3.39vw;
    }
    .selection-2 .list_div:hover h4 {
      margin-bottom: 1.4vh;
      font-size: 1.3vw;
    }
    .selection-2 .list_div:hover p {
      display: block;
      font-size: 1.04vw;
    }
  }
</style>
