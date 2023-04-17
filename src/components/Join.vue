<template>
  <div class="join">
    <div class="pc">
      <div class="selection selection-1">
        <app-header></app-header>
        <div class="cont">
          <div class="cons">
            <h1>大众创业，万众创新！</h1>
            <p>物联网智能净水器一站式解决方案<br/>
               支持多种计费方式，满足您的所有商业模式</p>
          </div>
        </div>
      </div>
      <div class="selection selection-2">
        <div class="cont">
          <div class="cont_bg"></div>
          <div class="list_div">
            <div class="list_div_bg bg_01"></div>
            <div class="list_div_con">
              <div class="_cons">
                <img src="../assets/39.svg" alt="">
                <p>一、加盟条件<br/>加盟费39800元</p> 
              </div>
            </div>
            <div class="right_p">
              1、给到1000台机器<br/>
              A、首发21台，一台为样机，公司并充好1200元包年水费。每装完并激活15台后公司补充15台到经销商处。<br/>
              B、给相应的助推产品（跟据公司活动而定，如小宝机器人，驼绒被，电话卡等）<br/>
              C、地推帐蓬、宣传单和产品介绍手册、马夹、水检测设备1套）<br/>
              D、装完1000台水机，加盟费等额退还。（等同零投资、0加盟）<br/>
              附：<br/>
              1、39800元加盟费也可以理解为押金，防止经销商拿到机器不装或损坏而给公司带来损失<br/>
              2、39800元必须把1000台把机器装完才可退目的为的是促使大家用心把机器装完，不是为了拉人头）
            </div>
          </div>
          <div class="list_div list_div_c">
            <div class="list_div_bg bg_02"></div>
            <div class="list_div_con">
              <div class="_cons">
                <img src="../assets/40.svg" alt="">
                <p>二、顾客装机<br/>分为两个套餐</p>
              </div>
            </div>
            <div class="right_p">
              1、流量套餐<br/>
              A：充980元<br/> 
              送3500升净水流量（平均。 每升0.28元。相当于195桶大的桶装水。可节约：195x8元/桶=1560元－980元=680元<br/>
              B：充1280元<br/>
              送5000升净水流量（平均0.25元/升，相当于278桶大的桶装水。可节约：278x8元/<br/>桶=2224元－1280元=944元）另送100电话卡3张<br/>
              C：充1680元<br/>
              8000升净水流量（平均0.21元/升，相当445桶大的桶装水。可节约445x8元/桶=3560元一1680元=1880元。<br/>
              另加送a、10000元包年电话卡 b、吴秀波代言的驼绒被价值1580元<br/>
              (二选一)<br/>
              注：以上套餐均不限使用期限。<br/>
              <br/>
              2、时长套餐<br/>
                包年方案：<br/>
              包年1200元，不限流量，想怎么用就怎么用。主要针对店面、公司和使用量较大的家庭。<br/>
            </div>
          </div>
          <div class="list_div">
            <div class="list_div_bg bg_03"></div>
            <div class="list_div_con">
              <div class="_cons">
                <img src="../assets/41.svg" alt="">
                <p>三、加盟商收益</p>
              </div>
            </div>
            <div class="right_p">
              1、装机收益<br/>
              机器是免费送的但是要顾客付初装员工成本180元／台<br/>
              a、自己安装180元/台x1000元=18万<br/>
              b、对接日日顺(海尔公司服务商－日日顺公司）每装1台80元／台。（180-80)=100元x1000=10万<br/>
              2、介绍加盟收益<br/>
              a、你可获得自己装机总流量30%的分佣<br/>
              平均按1280元／台x1000台x30%=38.4万<br/>
              b、可获得你一级经销商装机总流量10%的分佣<br/>
              平均按1280元／台x1000台X10%=12.8万<br/>
              c、可获得你二级经销商装机总流量5%的分佣<br/>
              平均按1280元/台x1000台x5%=6.4万<br/>
              注：每个经销商装完1000台可以继续装机。装机数量不限多劳多得。
            </div>
          </div>
        </div>
        <app-footer></app-footer>  
      </div>
    </div>
    <div class="mob">
      <div class="selection selection-1">
        <app-header></app-header>
        <div class="cont">
          <div class="cons">
            <h1>大众创业，万众创新！</h1>
            <p class="discr">物联网智能净水器一站式解决方案<br/>
               支持多种计费方式，满足您的所有商业模式</p>
            <button class="down-btn" @click="slideDown">
              <i class="icon-Group-47"></i>
            </button>
          </div>
        </div>
      </div>
      <div class="selection selection-2">
        <div class="cont">
          <div class="list_div bg_01">
            <div class="list_div_">
              <img src="../assets/39.svg" alt="">
              <p>一、加盟条件<br/>加盟费39800元</p> 
              <p class="blue">1、给到1000台机器</p>
              <div class="right_p">
                A、首发21台，一台为样机，公司并充好1200元包年水费。每装完并激活15台后公司补充15台到经销商处。<br/>
                B、给相应的助推产品（跟据公司活动而定，如小宝机器人，驼绒被，电话卡等）<br/>
                C、地推帐蓬、宣传单和产品介绍手册、马夹、水检测设备1套）<br/>
                D、装完1000台水机，加盟费等额退还。（等同零投资、0加盟）<br/>
              </div>
              <p class="blue">附：</p>
              <div class="right_p">
                1、39800元加盟费也可以理解为押金，防止经销商拿到机器不装或损坏而给公司带来损失<br/>
                2、39800元必须把1000台把机器装完才可退目的为的是促使大家用心把机器装完，不是为了拉人头）
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="selection selection-2">
        <div class="cont">
          <div class="list_div bg_02">
            <div class="list_div_">
              <div class="list_div_con">
                <div class="_cons">
                  <img src="../assets/40.svg" alt="">
                  <p>二、顾客装机<br/>分为两个套餐</p>
                </div>
              </div>
              <p class="blue">1、流量套餐</p>
              <div class="right_p">
                A：充980元<br/> 
                送3500升净水流量（平均。 每升0.28元。相当于195桶大的桶装水。可节约：195x8元/桶=1560元－980元=680元<br/>
                B：充1280元<br/>
                送5000升净水流量（平均0.25元/升，相当于278桶大的桶装水。可节约：278x8元/<br/>桶=2224元－1280元=944元）另送100电话卡3张<br/>
                C：充1680元<br/>
                8000升净水流量（平均0.21元/升，相当445桶大的桶装水。可节约445x8元/桶=3560元一1680元=1880元。<br/>
                另加送a、10000元包年电话卡 b、吴秀波代言的驼绒被价值1580元<br/>
                (二选一)<br/>
                注：以上套餐均不限使用期限。<br/>
              </div>
              <p class="blue">2、时长套餐</p>
              <div class="right_p">
                包年方案：<br/>
                包年1200元，不限流量，想怎么用就怎么用。主要针对店面、公司和使用量较大的家庭。
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="selection selection-2">
        <div class="cont">
          <div class="list_div bg_03">
            <div class="list_div_">
              <div class="list_div_con">
                <div class="_cons">
                  <img src="../assets/41.svg" alt="">
                  <p>三、加盟商收益</p>
                </div>
              </div>
              <p class="blue">1、装机收益</p>
              <div class="right_p">
                机器是免费送的但是要顾客付初装员工成本180元／台<br/>
                a、自己安装180元/台x1000元=18万<br/>
                b、对接日日顺(海尔公司服务商－日日顺公司）每装1台80元／台。（180-80)=100元x1000=10万
              </div>
              <p class="blue">2、介绍加盟收益</p>
              <div class="right_p">
                a、你可获得自己装机总流量30%的分佣<br/>
                平均按1280元／台x1000台x30%=38.4万<br/>
                b、可获得你一级经销商装机总流量10%的分佣<br/>
                平均按1280元／台x1000台X10%=12.8万<br/>
                c、可获得你二级经销商装机总流量5%的分佣<br/>
                平均按1280元/台x1000台x5%=6.4万<br/>
                注：每个经销商装完1000台可以继续装机。装机数量不限多劳多得。
              </div>
            </div>
          </div>
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
  name: 'Join',
  data () {
    return {
    }
  },
  created() {
  },
  methods: {
    slideDown() {
      let downHeight = document.documentElement.clientHeight;
      window.scrollTo(0, downHeight);
      this.slideShow = true;
    }
  },
  mounted() {
    $('.list_div').hover(function() {
      var ind = $(this).index();
      $(this).siblings().find('.list_div_con').css({
        'opacity': 0
      });
      $('.cont_bg').animate();
      $('.cont_bg').addClass('bg_0' + ind);
      $(this).siblings('.list_div').find('.list_div_bg').fadeOut(1);
      
    }, function() {
      var ind = $(this).index();
      $(this).siblings().find('.list_div_con').css({
        'opacity': 1
      });
      $('.cont_bg').animate();
      $('.cont_bg').removeClass('bg_0' + ind);
    });

    $('.cont').hover(function() {
      $('.cont_bg').animate();
      $('.cont_bg').addClass('bg');
    }, function() {
      $('.cont_bg').animate();
      $('.cont_bg').removeClass('bg bg_01 bg_02 bg_03');
      $('.list_div').find('.list_div_con').css({
        'opacity': 1
      });
      $('.list_div').find('.list_div_bg').fadeIn(1);
      $('.list_div').find('.list_div_bg').animate({
        'display': 'block'
      });
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
    background: url('../assets/38.jpg') left center no-repeat;
    background-size: cover;
  }
  .selection-1 .cont {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
  .selection-1 h1 {
    padding-left: 3vw;
    margin-bottom: 4.17vh;
    color: #FFFFFF;
    text-align: center;
    font-size: 3.39vw;
    font-weight: 600;
  }
  .selection-1 p {
    color: #58B2FF;
    text-align: center;
    line-height: 3.18vw;
    font-size: 1.82vw;
  }

  /*selection-2*/
  .selection-2 {
    width: 100%;
    height: 100vh;
    overflow: hidden;
  }
  .selection-2 .cont {
    position: relative;
    display: flex;
    justify-content: center;
    height: 78.8vh;
    overflow: hidden;
  }
  .selection-2 .list_div {
    display: flex;
    justify-content: center;
    align-items:center;
    width: 33.33vw;
    cursor: pointer;
    -webkit-transition: all 3s ease-in-out;
    transition: all 3s ease-in-out;
  }
  .selection-2 .list_div_c {
    border-right: 1px solid rgba(115, 115, 115, 0.5);
    border-left: 1px solid rgba(115, 115, 115, 0.5);
  }
  .selection-2 .list_div_con {
    height: 22%;  
  }
  .selection-2 .list_div:hover .list_div_con {
    -webkit-transition: opacity 2s ease-in-out;
    transition: opacity 2s ease-in-out;
  }

  .selection-2 .bg_01 {
    background: url('../assets/42.jpg') left center no-repeat;
    background-size: cover;
  }
  .selection-2 .bg_02 {
    background: url('../assets/43.jpg') center center no-repeat;
    background-size: cover;
  }
  .selection-2 .bg_03 {
    background: url('../assets/44.jpg') right center no-repeat;
    background-size: cover;
  }
  .selection-2 .list_div img {
    display: block;
    width: 4.06vw;
    height: 4.06vw;
    margin: 0 auto 2.19vh;
  }
  .selection-2 .list_div p {
    color: #FFFFFF;
    text-align: center;  
    font-size: 1.82vw;
  }

  .selection-2 .right_p {
    position: absolute;
    left: 40.83vw;
    top: 0;
    display: flex;
    justify-content: center;
    align-items:center;
    height: 100%;
    color: #FFFFFF;
    line-height: 2.3vw;
    font-size: 1.04vw;
    opacity: 0;
    z-index: -1;
  }
  
  .cont_bg {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    -webkit-transform: scale(1);
    transform: scale(1);
    -webkit-transform-origin: 50%;
    transform-origin: 50%;
  }
  .list_div_bg {
    position: absolute;
    left: 0;
    top: 0;
    width: 33.33%;
    height: 100%;
    z-index: -2;
  } 
  .list_div_bg.bg_01 {
    left: 0;
  }
  .list_div_bg.bg_02 {
    left: 33.33%;
  }
  .list_div_bg.bg_03 {
    left: 66.66%;
  }
  .cont_bg.bg_01, .cont_bg.bg_02, .cont_bg.bg_03, .cont_bg.bg {
    -webkit-transform: scale(1.2);
    transform: scale(1.2);
    -webkit-transform-origin: 50%;
    transform-origin: 50%;
    -webkit-transition: all 4s ease-in-out;
    transition: all 4s ease-in-out;
  }
  
  @media screen and (max-width: 750px) { 
    .selection-1 {
      background: url('../assets/015.jpg') center center no-repeat;
      background-size: cover;
    }
    .selection-1 h1 {
      padding-left: 3vw;
      margin-bottom: 2.85vh;
      font-size: 7.47vw;
    }
    .selection-1 p {
      line-height: 6.18vw;
      font-size: 4.27vw;
    }
    .selection-1 .discr {
      position: relative;
      width: 88%;
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

    .selection-2 {
      height: auto;
    }
    .selection-2 .cont {
      height: 100%;
    }
    .selection-2 .con_ {
      width: 100%;
    }
    .selection-2 .list_div img {
      width: 20.8vw;
      height: 20.8vw;
      margin: 0 auto 3.6vh;
    }
    .selection-2 .list_div.bg_01 {
      width: 100%;
      height: 112.74vh;
    }
    .selection-2 .list_div.bg_02 {
      width: 100%;
      height: 138.58vh;
    }
    .selection-2 .list_div.bg_03 {
      width: 100%;
      height: 108.4vh;
    }
    .selection-2 .bg_01 {
      background: url('../assets/016.jpg') left center no-repeat;
      background-size: cover;
    }
    .selection-2 .bg_02 {
      background: url('../assets/017.jpg') center center no-repeat;
      background-size: cover;
    }
    .selection-2 .bg_03 {
      background: url('../assets/018.jpg') right center no-repeat;
      background-size: cover;
    }
    .selection-2 .right_p {
      position: static;
      height: auto;
      line-height: 2.3vw;
      font-size: 1.04vw;
      opacity: 1;
      z-index: 1;
    }
    .selection-2 .list_div p {
      margin-bottom: 6.75vh;
      font-size: 5.33vw;
    }
    .selection-2 .list_div .blue {
      width: 80%;
      margin: 0 auto;
      color: #58B2FF;
      text-align: left;
      line-height: 7.2vw;
      font-size: 4vw;
      font-weight: 600;
    }
    .selection-2 .list_div .right_p {
      width: 80%;
      margin: 0 auto;
      font-size: 3.2vw;
      line-height: 7.2vw;
    }
  }

  @media screen and (min-width: 751px) {
    .selection-2 .list_div:hover .right_p {
      opacity: 1;
      -webkit-transition: all 2s ease-in-out;
      transition: all 2s ease-in-out;
    }
    .selection-2 .list_div:hover .list_div_con {
      position: absolute;
      left: 10%;
      top: 0;
      display: flex;
      justify-content: center;
      align-items:center;
      height: 100%;
    }
  }

</style>
