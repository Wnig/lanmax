<template>
  <div class="home">
    <div class="pc">
      <div class="selection selection-1">
        <video class="video1" src="../assets/video_02.mp4" autoplay="" loop=""></video>
        <div class="masks"></div>
        <app-header></app-header>
        <div class="cont">
          <h1>蓝密码物联网+智能净水共享时代</h1>
          <h3>大健康+物联网+共享经济</h3>
          <p>1.无需高昂购机费     2.拒绝更换滤芯费     3.砍掉日常维护费</p>
          <img class="word" src="../assets/8.png" alt="">
          <button class="down-btn" @click="slideDown">
            <i class="icon-Group-47"></i>
          </button>
          <img class="right_img" src="../assets/7.png" alt="">
        </div>
      </div>
      <div class="selection selection-2">
        <video class="video1" src="../assets/video_01.mp4" autoplay="" loop=""></video>
        <div class="cont clearfix">
          <div class="cont_">
            <div id="videoPlay">
              <img @click="play" v-show="isPlay" class="playbtn" src="../assets/10.svg" alt="">
              <video @click="play" @timeupdate="timeupdate" ref='video' class="video" src="../assets/video_03.mp4">
                  不支持播放
              </video>
              <div class="control-btn">
                <div class="control-con">
                  <span class="start">{{start}}</span>
                  <span id="title"></span>
                  <div ref='pro' id="progress">
                      <div :style="{width:prog + '%'}"></div>
                      <span id="bar" :style="{left: barLeft + '%'}"></span>
                  </div>
                  <span class="end">{{end}}</span>
                  <i class="icon-11" @click="fullScreen"></i>
                </div>
              </div>
            </div>
            <div class="right-con">
              <h1>项目<br/>起源</h1>
              <p>随着生活水平不断提高，人们的健康意识也逐渐强化，微生物、杂质、重金属、消毒副产品等水污染、水二次污染不断威胁用水安全，引起急、慢性身体中毒现象，长期饮用含有消毒副产物的水，有可能会导致心脑血管疾病、氟中毒、肿瘤的发生。<br/>
              <br/>
              蓝密码致力于净化水研究，提出智能+物联网+净水服务新模式。蓝密码水管家净水系统采用国际先进的RO反渗透净水原理，植入核心物联网控制技术，采用物联网云计算推出物联网智能饮水机，打造物联网智能健康净水服务平台，形成了从传感器、净水机、智能净水机方案、净水售后服务、净水大数据的完善服务系统，掀起了互联网+分享+服务模式热潮。<br/>
              蓝密码智能云平台，积极响应国家“大众创业、万众创新”的方针，为平台、运营商和用户之间提供智能净水服务。平台全网互联，不受区域限制，真正做到资源共享服务平台。</p>
            </div>
          </div>
        </div>
      </div>
      <div class="selection selection-3">
        <h2 class="title">平台优势</h2>
        <p class="discr">用户只需将手机绑定企业APP，就能轻松的喝到纯净的健康之水，设备免费、流量计费、免费售后服务、免费更换滤芯等终身免费服务，平台运营商只需负责前期的终端用户开拓，后期的设备安装、售后服务等，均由蓝密码智能云平台负责，让运营商实现无忧经营、轻松盈利。</p>
        <div id="swiperCon" class="swiper-container clearfix">
          <div class="swiper-wrapper">
            <div class="swiper-slide">
              <div class="cont clearfix">
                <transition name="fade" enter-active-class="fadeInUp" leave-active-class="fadeOutUp">
                  <img v-if="show" class="user_img" src="../assets/13.svg" alt="">
                </transition>
                <transition name="fade" enter-active-class="fadeInRight" leave-active-class="fadeOutRight">
                  <img v-if="show" class="right_img" src="../assets/14.jpg" alt="">
                </transition>
                <div class="project_jq3d">
                  <div class="project">
                    <div class="project_card">
                        <div class="project_detail">
                          <transition name="fade" enter-active-class="fadeInRight" leave-active-class="fadeOutRight">
                            <h2 v-if="show" class="project_title"><i class="icon-12"></i>用户端</h2>
                          </transition>
                          <transition name="fade" enter-active-class="fadeInRight" leave-active-class="fadeOutRight">
                            <p v-if="show" class="project_category">智能净水云平台，简单操作，全方位监控数据实时获取，用户更省心！</p>
                          </transition>
                          <transition name="fade" enter-active-class="fadeInLeft" leave-active-class="fadeOutLeft">
                            <p v-if="show" class="project_p">
                              1.支持微信平台<br/>
                              2.手机实时查看水机状况<br/>
                              3.用户永远不用操心，第一时间智能提醒<br/>
                              4.滤芯更换及时提醒，在线下单快递到家<br/>
                              5.用水数据明明白白<br/>
                              6.在线充值缴费、购买套餐，即时到账
                            </p>
                          </transition>
                        </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="swiper-slide">
              <div class="cont clearfix">
                <transition name="fade" enter-active-class="fadeInUp" leave-active-class="fadeOutUp">
                  <img v-if="show_02" class="user_img" src="../assets/15.svg" alt="">
                </transition>
                <transition name="fade" enter-active-class="fadeInRight" leave-active-class="fadeOutRight">
                  <img v-if="show_02" class="right_img" src="../assets/16.jpg" alt="">
                </transition>
                <div class="project_jq3d">
                  <div class="project">
                    <div class="project_card">
                      <div class="project_detail">
                        <transition name="fade" enter-active-class="fadeInRight" leave-active-class="fadeOutRight">
                          <h2 v-if="show_02" class="project_title"><i class="icon-12"></i>经销商端</h2>
                        </transition>
                        <transition name="fade" enter-active-class="fadeInRight" leave-active-class="fadeOutRight">
                          <p v-if="show_02" class="project_category">客户管理、设备监控、大数据服务、结算分成轻松搞定运营商生意轻松开展！</p>
                        </transition>
                        <transition name="fade" enter-active-class="fadeInLeft" leave-active-class="fadeOutLeft">
                          <p v-if="show_02" class="project_p">
                            1.在线客户服务，拉近客户距离<br/>
                            2.智能云平台，管理所需要的都在这里<br/>
                            3.什么时间做什么事，系统一一提醒<br/>
                            4.经营不再只凭感觉经验，丰富数据给你准确依据<br/>
                            5.自动酬金结算，定期生成结算单
                          </p>
                        </transition>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="swiper-pagination"></div>
          <div class="pre_next">
            <i class="icon-arrow-left2 left_ico"></i>Next <i class="icon-arrow-right2 right_ico"></i>  
          </div>
        </div>
      </div>
      <div class="selection selection-4">
        <div class="discr-con">
          <h2 class="title">蓝密码市场优势</h2>
          <p class="discr">我们不仅是净水器的生产商，还是净化水的服务商！</p>
        </div>
        <div class="cont">
          <img src="../assets/18.png" alt="">
        </div>
      </div>
      <div class="selection selection-5">
        <div class="discr-con">
          <h2 class="title">市场需求</h2>
          <p class="discr">为什么需要蓝密码智能净水云平台？</p>
        </div>
        <div class="cont">
          <div class="list_div list_01">
            <div class="list_div_con">
              <img src="../assets/20.svg" alt="">
              <p>产品升级换代</p>
            </div>
          </div>
          <div class="list_div list_02">
            <div class="list_div_con">
              <img src="../assets/21.svg" alt="">
              <p>创新商业模式</p>
            </div>
          </div>
          <div class="list_div list_03">
            <div class="list_div_con">
              <img src="../assets/22.svg" alt="">
              <p>客户体验升级</p>
            </div>
          </div>
          <div class="list_div list_04">
            <div class="list_div_con">
              <img src="../assets/23.svg" alt="">
              <p>营销成本降低</p>
            </div>
          </div>
        </div>
      </div>
      <div class="selection selection-6">
        <div class="discr-con">
          <h2 class="title">应用场景</h2>
        </div>
        <div class="cont">
          <div class="list_div">
            <img src="../assets/25.jpg" alt="">
            <p>公司团体</p>
          </div>
          <div class="list_div">
            <img src="../assets/26.jpg" alt="">
            <p>餐饮机构</p>
          </div>
          <div class="list_div">
            <img src="../assets/27.jpg" alt="">
            <p>多口之家</p>
          </div>
          <div class="list_div">
            <img src="../assets/28.jpg" alt="">
            <p>单身贵族</p>
          </div>
        </div>
      </div>
      <div class="selection selection-7">
        <div class="sel-con">
          <div class="discr-con">
            <h2 class="title">盈利方式</h2>
            <p class="discr">支持多种计费方式，满足您所有的商业模式需求</p>
          </div>
          <div class="cont">
            <div class="list_div">
              <div class="list_div_con">
                <img src="../assets/30.svg" alt="">
                <p>产品升级换代</p>
              </div>
            </div>
            <div class="list_div">
              <div class="list_div_con">
                <img src="../assets/31.svg" alt="">
                <p>创新商业模式</p>
              </div>
            </div>
            <div class="list_div">
              <div class="list_div_con">
                <img src="../assets/32.svg" alt="">
                <p>客户体验升级</p>
              </div>
            </div>
            <div class="list_div">
              <div class="list_div_con">
                <img src="../assets/33.svg" alt="">
                <p>营销成本降低</p>
              </div>
            </div>
          </div>
        </div>
        <app-footer></app-footer>
      </div>
    </div>
    <div class="mob">
      <div class="selection selection-1">
        <img class="video1" src="../assets/video_02.gif"></img>
        <div class="masks"></div>
        <app-header></app-header>
        <div class="cont">
          <div class="cont_">
            <h1>物联网<br/>智能净水共享时代</h1>
            <h3>大健康+物联网+共享经济</h3>
            <p>1.无需高昂购机费     2.拒绝更换滤芯费<br/>     3.砍掉日常维护费</p>
            <img class="word" src="../assets/8.png" alt="">
            <img class="right_img" src="../assets/7.png" alt="">
            <button class="down-btn" @click="slideDown">
              <i class="icon-Group-47"></i>
            </button>
          </div>
        </div>
      </div>
      <div class="selection selection-2">
        <img class="video1" src="../assets/video_01.gif"></img>
        <div class="cont clearfix">
          <div class="cont_">
            <div id="videoPlay">
              <img @click="play" v-show="isPlay" class="playbtn" src="../assets/10.svg" alt="">
              <video @click="play" @timeupdate="timeupdate" ref='video02' class="video" src="../assets/video_03.mp4">
                  不支持播放
              </video>
              <div class="control-btn">
                <div class="control-con">
                  <span class="start">{{start}}</span>
                  <span id="title"></span>
                  <div ref='pro' id="progress">
                      <div :style="{width:prog + '%'}"></div>
                      <span id="bar" :style="{left: barLeft + '%'}"></span>
                  </div>
                  <span class="end">{{end}}</span>
                  <i class="icon-11" @click="fullScreen"></i>
                </div>
              </div>
            </div>
            <div class="right-con">
              <h1>项目起源</h1>
              <p>随着生活水平不断提高，人们的健康意识也逐渐强化，微生物、杂质、重金属、消毒副产品等水污染、水二次污染不断威胁用水安全，引起急、慢性身体中毒现象，长期饮用含有消毒副产物的水，有可能会导致心脑血管疾病、氟中毒、肿瘤的发生。<br/>
              <br/>
              蓝密码致力于净化水研究，提出智能+物联网+净水服务新模式。蓝密码水管家净水系统采用国际先进的RO反渗透净水原理，植入核心物联网控制技术，采用物联网云计算推出物联网智能饮水机，打造物联网智能健康净水服务平台，形成了从传感器、净水机、智能净水机方案、净水售后服务、净水大数据的完善服务系统，掀起了互联网+分享+服务模式热潮。<br/>
              蓝密码智能云平台，积极响应国家“大众创业、万众创新”的方针，为平台、运营商和用户之间提供智能净水服务。平台全网互联，不受区域限制，真正做到资源共享服务平台。</p>
            </div>
          </div>
        </div>
      </div>
      <div class="selection selection-3">
        <div class="conts">
          <div class="conts_">
            <h2 class="title">平台优势</h2>
            <p class="discr">用户只需将手机绑定企业APP，就能轻松的喝到纯净的健康之水，设备免费、流量计费、免费售后服务、免费更换滤芯等终身免费服务，平台运营商只需负责前期的终端用户开拓，后期的设备安装、售后服务等，均由蓝密码智能云平台负责，让运营商实现无忧经营、轻松盈利。</p>
            <div id="swiper" class="swiper-container clearfix">
              <div class="swiper-wrapper">
                <div class="swiper-slide">
                  <div class="cont clearfix">
                    <div class="cont_">
                      <div class="right_img img_01"></div>
                      <div class="project_detail">
                        <h2 class="project_title"><i class="icon-12"></i>用户端</h2>
                        <p class="project_category">智能净水云平台，简单操作，全方位监控数据实时获取，用户更省心！</p>
                        <p class="project_p">
                          1.支持微信平台<br/>
                          2.手机实时查看水机状况<br/>
                          3.用户永远不用操心，第一时间智能提醒<br/>
                          4.滤芯更换及时提醒，在线下单快递到家<br/>
                          5.用水数据明明白白<br/>
                          6.在线充值缴费、购买套餐，即时到账
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="swiper-slide">
                  <div class="cont clearfix">
                    <div class="cont_">
                      <div class="right_img img_02"></div>
                      <div class="project_detail">
                        <h2 class="project_title"><i class="icon-12"></i>经销商端</h2>
                        <p class="project_category">客户管理、设备监控、大数据服务、结算分成轻松搞定运营商生意轻松开展！</p>
                        <p class="project_p">
                          1.在线客户服务，拉近客户距离<br/>
                          2.智能云平台，管理所需要的都在这里<br/>
                          3.什么时间做什么事，系统一一提醒<br/>
                          4.经营不再只凭感觉经验，丰富数据给你准确依据<br/>
                          5.自动酬金结算，定期生成结算单
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="swiper-pagination"></div>
            </div>
          </div>
        </div>
      </div>
      <div class="selection selection-4">
        <div class="discr-con">
          <h2 class="title">蓝密码市场优势</h2>
          <p class="discr">我们不仅是净水器的生产商<br/>还是净化水的服务商！</p>
        </div>
        <div class="cont">
          <img src="../assets/009.png" alt="">
        </div>
      </div>
      <div class="selection selection-5">
        <div class="discr-con">
          <h2 class="title">市场需求</h2>
          <p class="discr">为什么需要<br/>蓝密码智能净水云平台？</p>
        </div>
        <div class="cont">
          <div class="list_div list_01">
            <div class="list_div_con">
              <img src="../assets/20.svg" alt="">
              <p>产品升级换代</p>
            </div>
          </div>
          <div class="list_div list_02">
            <div class="list_div_con">
              <img src="../assets/21.svg" alt="">
              <p>创新商业模式</p>
            </div>
          </div>
          <div class="list_div list_03">
            <div class="list_div_con">
              <img src="../assets/22.svg" alt="">
              <p>客户体验升级</p>
            </div>
          </div>
          <div class="list_div list_04">
            <div class="list_div_con">
              <img src="../assets/23.svg" alt="">
              <p>营销成本降低</p>
            </div>
          </div>
        </div>
      </div>
      <div class="selection selection-6">
        <div class="discr-con">
          <h2 class="title">应用场景</h2>
        </div>
        <div id="swiper02" class="swiper-container clearfix">
          <div class="swiper-wrapper">
            <div class="swiper-slide">
              <div class="list_div">
                <img src="../assets/25.jpg" alt="">
                <p>公司团体</p>
              </div>
            </div>
            <div class="swiper-slide">
              <div class="list_div">
                <img src="../assets/26.jpg" alt="">
                <p>餐饮机构</p>
              </div>
            </div>
            <div class="swiper-slide">
              <div class="list_div">
                <img src="../assets/27.jpg" alt="">
                <p>多口之家</p>
              </div>
            </div>
            <div class="swiper-slide">
              <div class="list_div">
                <img src="../assets/28.jpg" alt="">
                <p>单身贵族</p>
              </div>
            </div>
          </div>
          <div class="swiper-pagination"></div>
        </div>
      </div>
      <div class="selection selection-7">
        <div class="sel-con">
          <div class="discr-con">
            <h2 class="title">盈利方式</h2>
            <p class="discr">支持多种计费方式，满足您<br/>所有的商业模式需求</p>
          </div>
          <div class="cont">
            <div class="list_div">
              <div class="list_div_con">
                <div class="list_div_con_">
                  <img src="../assets/30.svg" alt="">
                  <p>产品升级换代</p>
                </div>
              </div>
            </div>
            <div class="list_div">
              <div class="list_div_con">
                <div class="list_div_con_">
                  <img src="../assets/31.svg" alt="">
                  <p>创新商业模式</p>
                </div>
              </div>
            </div>
            <div class="list_div">
              <div class="list_div_con">
                <div class="list_div_con_">
                  <img src="../assets/32.svg" alt="">
                  <p>客户体验升级</p>
                </div>
              </div>
            </div>
            <div class="list_div">
              <div class="list_div_con">
                <div class="list_div_con_">
                  <img src="../assets/33.svg" alt="">
                  <p>营销成本降低</p>
                </div>
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
import '../../static/js/jquery.hover3d.min.js'
import Header from './Header'
import Footer from './Footer'

export default {
  name: 'Home',
  data () {
    return {
      prog: '0',
      barLeft: '0',
      isPlay: true,
      start: '0:00',
      end: '0:00',
      show: false,
      show_02: false,
    }
  },
  created() {
    this.show = true;
  },
  methods: {
    play() {
      if(this.isPlay) {
        this.$refs.video.play();
        this.$refs.video02.play();
        this.isPlay = false;
      } else {
        this.$refs.video.pause();
        this.$refs.video02.pause();
        this.isPlay = true;
      };
    },
    timeupdate() {
      var time = parseInt(this.$refs.video.currentTime);
      var time = parseInt(this.$refs.video02.currentTime);
      let min = parseInt(time / 60);
      let sec = parseInt(time % 60) > 9 ? parseInt(time % 60) : '0' + parseInt(time % 60);
      this.start = min + ':' + sec;

      var times = parseInt(this.$refs.video.duration);
      var times = parseInt(this.$refs.video02.duration);
      let mins = parseInt(times / 60);
      let secs = parseInt(times % 60) > 9 ? parseInt(times % 60) : '0' + parseInt(times % 60);
      this.end = mins + ':' + secs;

      this.prog = (time / times) * 100;
      this.barLeft = (time / times) * 100;

      if(time == times) {
        this.isPlay = true;
        this.start = '0:00';
        this.end = '0:00';
        this.prog = 0;
        this.barLeft = 0;
      };
    },
    //全屏显示
    fullScreen() {
      function launchFullScreen(element) {  
        if(element.requestFullscreen) {  
          element.requestFullscreen();  
        } else if(element.mozRequestFullScreen) {  
          element.mozRequestFullScreen();  
        } else if(element.webkitRequestFullscreen) {  
          element.webkitRequestFullscreen();  
        } else if(element.msRequestFullscreen) {  
          element.msRequestFullscreen();  
        }  
      }
      // 某个元素  
      let Width = document.documentElement.clientWidth;
      if(Width > 750) {
        launchFullScreen(this.$refs.video); 
      } else {
        launchFullScreen(this.$refs.video02); 
      }
    },
    slideDown() {
      let downHeight = document.documentElement.clientHeight || document.body.clientHeight;
      window.scrollTo(0, downHeight);
      this.slideShow = true;
    }
  },
  mounted() {
    $(document).ready(function(){
      $(".project_jq3d").hover3d({
        selector: ".project",
        shine: true,
      });
    });

    let _this = this;
    let swiperCon = new Swiper('#swiperCon', {
      direction: 'vertical',
      slidesPerView: 1,
      spaceBetween: 800,
      speed: 10,
      mousewheelControl: true,
      releaseOnEdges: true,
      paginationClickable: true,
      pagination: '.swiper-pagination',
      paginationType : 'custom',
      paginationCustomRender: function (swiper, current, total) {
        return '<span style="color: #58B2FF;font-size: 2.34vw;" class="swiper-pagination-current">0'+ current +'</span>' + ' / ' + '<span style="font-size: 1.15vw;" class="swiper-pagination-total">0'+ total + '</span>';
      },
      prevButton: '.left_ico',
      nextButton: '.right_ico',
      onSlideChangeEnd:function(swiper){
        if(swiper.activeIndex == 0) {
          _this.show = true;
          _this.show_02 = false;
        } else {
          _this.show = false;
          _this.show_02 = true;
        }
      },
    });
    let swiper = new Swiper('#swiper, #swiper02', {
      loop: true, 
      slidesPerView: 1,
      spaceBetween: 100,
      speed: 1000,
      mousewheelControl: true,
      releaseOnEdges: true,
      paginationClickable: true,
      pagination: '.swiper-pagination',
    });

  },
  components: {
    'app-header': Header,
    'app-footer': Footer
  }
}
</script>

<style scoped>

  video::-webkit-media-controls{
    display:none !important;
  }
  :-webkit-full-screen video {
    width: 100%;
    height: 100%;
  }
  :-moz-full-screen video {
    width: 100%;
    height: 100%;
  }

  /*selection-1*/
  .selection-1 {
    position: relative;
  }
  .selection-1 .cont {
    position: absolute;
    left: 0;
    top: 0;
    width: 91.2vw;
    height: 70.74vh;
    padding-top: 29.26vh;
    margin-left: 8.8vw;
  }
  .masks {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: url('../assets/bg-dot.png') repeat;
  }
  .selection-1 h1 {
    margin-bottom: 1.57vh;
    color: #FFFFFF;
    font-size: 3.39vw;
    font-weight: 600;
  }
  .selection-1 h3 {
    margin-bottom: 6.2vh;
    color: #58B2FF;
    font-size: 1.82vw;
  }
  .selection-1 p {
    margin-bottom: 2.87vh;
    color: #FFFFFF;
    line-height: 1.3vw;
    font-size: 1.04vw;
  }
  .selection-1 .word {
    display: block;
    width: 37.92vw;
  }
  .selection-1 .right_img {
    position: absolute;
    right: 6.15vw;
    bottom: 0;
    width: 44.43vw;
  }

  /*selection-2*/
  .selection-2 {
    position: relative;
  }
  
  .video1 {
    position: relative;
    z-index: -1;
    width: 100%;
    height: 100%;
    -o-object-fit: fill;
    object-fit: fill;
  }

  .selection-2 .cont {
    position: absolute;
    left: 0;
    top: 0;
    align-items: center;
    display: inline-flex;
    height: 100%;
    width: 100%;
    background: rgba(88, 178, 255, 0.78);
    z-index: 1;
  }
  .selection-2 .cont_ {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  #videoPlay {
    float: left;
    position: relative;
    width: 40.57vw;
    margin-right: 3.75vw;
    font-size: 0;
    overflow: hidden;
  }
  
  .video {
    width: 100%;
    height: 27.44vw;
    cursor: pointer;
  }

  .control-btn {
    position: absolute;
    bottom: 0;
    left: 0;
    display: flex;
    justify-content: center;
    width: 100%; 
    height: 7.41vh;
    background-color: rgba(0, 0, 0, 1);
    z-index: 99999999999;
  }
  
  .control-con {
    align-items: center;
    display: inline-flex;
  }
  
  .start {
    margin-right: 0.6vw;
    color: #fff;
    font-size: 0.94vw;
  } 
  .end {
    margin-right: 3.07vw;
    color: #fff;
    font-size: 0.94vw;
  }

  #progress {
    position: relative;
    width: 25.26vw;
    height: 0.16vw;
    margin-right: 0.94vw;
    background-color: #CCCCCC;
    cursor: pointer;
  }
  #progress div {
    position: absolute;
    left: 0;
    top: 0;
    height: 0.16vw;
    background-color: #fff;
  }
  #bar {
    position: absolute;
    left: 0%;
    top: -0.45vw;
    width: 0.89vw;
    height: 0.89vw;
    border: 0 solid #979797;
    border-radius: 50%;
    background: #5DBAE0;
    box-shadow: 0 0 4px 0 #5DBAE0;
  }
  
  .control-con i {
    font-size: 1.46vw;
    cursor: pointer;
  }

  .playbtn {
    position: absolute;
    margin: auto;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    width: 4.38vw;
    height: 4.38vw;
    z-index: 999999999999;
    cursor: pointer;
  }
  .selection-2 .right-con {
    float: left;
    width: 30.94vw;
  }
  .selection-2 .cont h1 {
    position: relative;
    margin-bottom: 3.07vh;
    color: #FFFFFF;
    line-height: 4vw;
    font-size: 3.43vw;
  }
  .selection-2 .cont p {
    color: #FFFFFF;
    line-height: 1.6vw;
    font-size: 1.04vw;
  }

  .selection-2 .cont h1:after {
    content: '';
    position: absolute;
    left: 0;
    bottom: 0.8vw;
    width: 70%;
    height: 0.31vw;
    font-size: 2vw;
    background: url('../assets/4.png') center center no-repeat;
    background-size: auto 100%;
  }

  /*selection-3*/
  .selection-3 {
    width: 100%;
    height: 100vh;
    overflow: hidden;
  }
  .selection-3 .title {
    color: #000;
  }
  .selection-3 .discr {
    color: #949494;
  }

  #swiperCon {
    height: 62.69vh;
    margin-right: 9.58vw;
    margin-top: 4.7vh;
    padding-left: 9.58vw;
  }

  /*hover3d*/
  .project_jq3d {
    position: absolute;
    left:0;
    right:0;
    top: 0;
    bottom: 0;
    margin: auto;
    width: 40.68vw;
    height: 27.97vw;
    z-index: 999999999999;
  }
  .project {
    width: 40.68vw;
    height: 27.97vw;
    box-shadow: 0 12px 31px 0 rgba(0,0,0,0.14);
    border-radius: 6px;
    /*background: rgba(255, 255, 255, 0.8);*/
    background: rgba(255, 255, 255, 0.85);
    /*background: url('../assets/blur.png') center center no-repeat;
    background-size: cover;*/
  }
  
  .project_card {
    padding: 3.65vw 4.84vw;
  }
  .project_title {
    margin-bottom: 1.3vw;
    color: #58B2FF;
    font-size: 1.82vw;
  }
  .project_title i {
    margin-right: 1.41vw;
  }
  .project_detail {
    
  }
  .project_category {
    position: relative;
    margin-bottom: 2.81vw;
    font-size: 1.46vw;
  }
  .project_category:after {
    content: '';
    position: absolute;
    left: 0;
    bottom: -1.35vw;
    width: 3.65vw;
    height: 0.31vw;
    font-size: 2vw;
    background: url('../assets/3.svg') left center no-repeat;
    background-size: auto 100%;
  }
  .project_p {
    font-size: 1.04vw;
    color: #949494;
    line-height: 1.77vw;
  }
  
  .selection-3 .title {
    padding-top: 4.22vh;
  }

  .user_img {
    float: left;
    height: 17.59vh;
    margin-top: 8.33vh;
  }

  .right_img {
    float: right;
    width: 25.31vw;
  }

  #swiperCon .swiper-container-horizontal>.swiper-pagination-bullets, #swiperCon .swiper-pagination-custom, .swiper-pagination-fraction {
    bottom: 4.7vh;
    left: 0;
    width: 30%;
  }

  .pre_next {
    position: absolute;
    left: 0;
    bottom: 0;
    width: 30%;
    text-align: center;
    line-height: 2vw;
    font-size: 1.3vw;
    z-index: 999999999;
  }
  .pre_next i {
    color: #A5A5A5;
    line-height: 2vw;
    font-size: 1.35vw;
    cursor: pointer;
  }
  .left_ico {
    margin-right: 1.82vw;
  } 
  .right_ico {
    margin-left: 1.82vw;
  }
  
  /*selection-4*/
  .selection-4 {
    position: relative;
    background: url('../assets/17.jpg') center center no-repeat;
    background-size: cover;
  }
  .selection-4 .discr-con {
    padding-top: 16.3vh;
  }
  .selection-4 h2, .selection-4 .discr {
    color: #fff;
  }
  .selection-4 .cont {
    margin: 10.19vh auto;
    text-align: center;
  }
  .selection-4 .cont img {
    display: block;
    width: 54.95vw;
    margin: 0 auto;
  }

  /*selection-5*/
  .selection-5 {
    position: relative;
    background: url('../assets/19.jpg') center center no-repeat;
    background-size: cover;
  }
  .selection-5 .discr-con {
    padding-top: 10.28vh;
  }
  .selection-5 .cont {

  }
  .selection-5 .list_div {
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 11.98vw;
    height: 11.98vw;
    border-radius: 50%;
    background: #FFFFFF;
    box-shadow: 0 9px 30px 0 rgba(0,0,0,0.18);
    cursor: pointer;
  }
  .selection-5 .list_div_con {

  }
  .selection-5 .list_div p {
    font-size: 1.3vw;
  }
  .selection-5 .list_div img {
    display: block;
    width: 4.06vw;
    margin: 0 auto 1.57vh;
  }
  .selection-5 .list_01 {
    left: 7.5vw;
    bottom: 20vh;
    -webkit-animation: float_01 2s ease-in-out infinite;
    -moz-animation: float_01 2s ease-in-out infinite;
    -ms-animation: float_01 2s ease-in-out infinite;
    -o-animation: float_01 2s ease-in-out infinite;
  }
  .selection-5 .list_02 {
    left: 28.96vw;
    bottom: 42.78vh;
    -webkit-animation: float_02 3s ease-in-out infinite;
    -moz-animation: float_02 3s ease-in-out infinite;
    -ms-animation: float_02 3s ease-in-out infinite;
    -o-animation: float_02 3s ease-in-out infinite;
  }
  .selection-5 .list_03 {
    left: 59.06vw;
    bottom: 42.78vh;
    -webkit-animation: float_03 4s ease-in-out infinite;
    -moz-animation: float_03 4s ease-in-out infinite;
    -ms-animation: float_03 4s ease-in-out infinite;
    -o-animation: float_03 4s ease-in-out infinite;
  }
  .selection-5 .list_04 {
    left: 80.83vw;
    bottom: 20vh;
    -webkit-animation: float_04 1.5s ease-in-out infinite;
    -moz-animation: float_04 1.5s ease-in-out infinite;
    -ms-animation: float_04 1.5s ease-in-out infinite;
    -o-animation: float_04 1.5s ease-in-out infinite;
  }

  /*selection-6*/
  .selection-6 {
    background: url('../assets/24.jpg') center center no-repeat;
    background-size: cover;
  }
  .selection-6 .discr-con {
    padding-top: 15vh;
  }
  .selection-6 .cont {
    display: flex;
    justify-content: center;
    padding-top: 6.96vh;
  }
  .selection-6 .list_div {
    width: 17.55vw;
    margin-right: 0.83vw;
    cursor: pointer;
    -webkit-transition: all 0.8s;
    transition: all 0.8s;
  }
  .selection-6 .list_div img {
    display: block;
    width: 100%;
  }
  .selection-6 .list_div p {
    color: #000000;
    text-align: center;
    line-height: 5.57vw;
    font-size: 1.82vw;
    background: #fff;
  }
  /*selection-7*/
  .selection-7 {
    background: #232526;
  }
  .selection-7 .sel-con {
    height: 78.7vh;
    background: url('../assets/29.jpg') center center no-repeat;
    background-size: cover;
  }
  .selection-7 .discr-con {
    padding-top: 12.78vh;
  } 
  .selection-7 .cont {
    display: flex;
    justify-content: center;
    padding-top: 11.3vh;
  }
  .selection-7 .list_div {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 11.98vw;
    height: 11.98vw;
    margin: 0 2.68vw;
    border-radius: 50%;
    background: #FFFFFF;
    box-shadow: 0 9px 30px 0 rgba(0,0,0,0.18);
    cursor: pointer;
    -webkit-transition: all 0.8s;
    transition: all 0.8s;
  }
  .selection-7 .list_div:hover {
    -webkit-transform: scale(1.15);
    transform: scale(1.15);
    -webkit-transition: all 0.8s;
    transition: all 0.8s;
  }
  .selection-7 .list_div img {
    display: block;
    width: 4.06vw;
    margin: 0 auto 1.57vh;
  }
  .selection-7 .list_div p {
    font-size: 1.46vw;
  }
  
  @media screen and (max-width: 750px) {
    .selection-1 {
      height: 100vh;
    }
    .selection-1 .cont {
      align-items: center;
      display: inline-flex;
      width: 100%;
      height: 86vh;
      padding-top: 16.5vh;
      margin: 0;
      text-align: center;
    }
    .selection-1 .cont_ {

    }
    .selection-1 h1 {
      position: relative;
      margin-bottom: 3.15vh;
      font-size: 7.47vw;
    }
    .selection-1 h1:after {
      position: absolute;
      content: "+";
      right: 35%;
      top: -5vw;
      color: #58B2FF;
    }
    .selection-1 h3 {
      margin-bottom: 1.35vh;
      font-size: 4.8vw;
    }
    .selection-1 p {
      text-align: center;
      margin-bottom: 3.75vh;
      line-height: 5.33vw;
      font-size: 3.2vw;
    }
    .selection-1 .word {
      display: block;
      width: 85.07vw;
      margin: 0 auto 5.55vh;
    }
    .selection-1 .right_img {
      position: static;
      display: block;
      width: 100%;
      height: auto;
      margin: 0 auto;
    }
  
    /*selection-2*/
    .selection-2 .video1 {
      width: 140%;
      height: 100%;
    }
    .selection-2 {
      overflow: hidden;
      height: 140.97vh;
    }
    .selection-2 .cont {
      position: absolute;
      left: 0;
      top: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 100%;
      padding: 0;
    }
    .selection-2 .cont_ {
      display: block;
      /*padding-top: 15vh;*/
    }
    #videoPlay {
      float: none;
      overflow: hidden;
      display: block;
      width: 85.8vw;
      margin: 0 auto 6.9vh;
      font-size: 0;
      box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.5);
    }
    #bar {
      position: absolute;
      left: 0%;
      top: -1.06vw;
      width: 2.13vw;
      height: 2.13vw;
    }
    .video {
      width: 85.87vw;
      height: 48.4vw;
      background: url('../assets/9.jpg') center center no-repeat;
      background-size: cover;
    }
    .selection-2 .right-con {
      float: none;
      width: 82.13vw;
      margin: 0 auto;
    }
    .selection-2 .cont h1 {
      margin-bottom: 8.1vh;
      text-align: center;
      line-height: 7vw;
      font-size: 6.67vw;
    }

    .selection-2 .cont h1:after {
      content: '';
      position: absolute;
      left: 0;
      bottom: -2.4vh;
      width: 100%;
      height: 0.8vw;
      font-size: 2vw;
    }
    .selection-2 .cont p {
      line-height: 6.67vw;
      font-size: 3.73vw;
    }
    .start {
      margin-right: 0.6vw;
      font-size: 3.2vw;
    } 
    .end {
      margin-right: 3.07vw;
      font-size: 3.2vw;
    }
    .control-con i {
      font-size: 4.46vw;
    }

    #progress {
      position: relative;
      width: 53.6vw;
      height: 0.27vw;
    }
    .playbtn {
      width: 9.6vw;
      height: 9.6vw;    
    }

    /*selection-3*/
    .selection-3 {
      height: auto;
      overflow: scroll;
    }
    .selection-3 .conts {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 150.28vh;
    }
    .selection-3 .conts_ {
      width: 95%;
    }
    .selection-3 .discr {
      width: 88%;
      text-indent: 2em;
      text-align: left;
    }
    #swiper {
      height: 101vh;
      margin: 5.25vh auto 0;
      padding: 0;
    }

    .right_img {
      float: none;
      width: 100%;
      height: 39.43vh;
      margin-bottom: 4vh;
      border-radius: 3px 3px 0 0;
    }
    .selection-3 .cont {
      justify-content: center;
      align-items: center;
      width: 88%;
      height: 97%;
      display: block;
      margin: 0 auto;
    }
    .img_01 {
      background: url('../assets/14.jpg') center center no-repeat;
      background-size: 100% auto;
    }
    .img_02 {
      background: url('../assets/16.jpg') center center no-repeat;
      background-size: 100% auto;
    }
    .project_title {
      width: 88%;
      margin: 0 auto 3.45vh;
      border-bottom: 0.2vh solid #efefef;
      text-align: center;
      line-height: 15.4vw;
      font-size: 7.33vw;
    }
    .project_category {
      width: 92%;
      margin: 0 auto 2.25vh;
      text-align: center;
      line-height: 6.67vw;
      font-size: 4.27vw;
    }
    .project_category:after {
        background: none;
    }
    .project_p {
      margin-bottom: 4.5vh;
      line-height: 1.77vw;
      text-align: center;
      line-height: 5.33vw;
      font-size: 3.2vw;
    }
    .selection-3 .cont_ {
      background: rgba(255, 255, 255, 0.89);
      box-shadow: 0 12px 31px 0 rgba(0,0,0,0.14);
      border-radius: 3px;
      height: 95%;
    }
    .selection-3 .project_detail {
      padding-bottom: 1vh;
    }
    
    /*selection-4*/
    .selection-4 {
      height: 112.89vh;
      background: url('../assets/008.jpg') center center no-repeat;
      background-size: cover;
    }
    .selection-4 .discr-con {
      padding-top: 7.5vh;
    }
    .selection-4 .cont img {
      width: 90.93vw;
      height: 74.66vh;
    }
    .selection-4 .cont {
      margin: 2.1vh auto;
    }

    /*selection-5*/
    .selection-5 {
      position: relative;
      height: 100.75vh;
      background: url('../assets/010.jpg') center center no-repeat;
      background-size: cover;
    }
    .selection-5 .discr-con {
      padding-top: 8.7vh;
    }

    .selection-5 .list_div {
      width: 26.61vw;
      height: 26.61vw;
    }
    .selection-5 .list_div img {
      width: 8.53vw;
      margin: 0 auto 1.57vh;
    }
    .selection-5 .list_div p {
      font-size: 3.2vw;
    }
    .selection-5 .list_01 {
      left: 3.47vw;
      bottom: 20.68vh;
    }
    .selection-5 .list_02 {
      left: 15.73vw;
      bottom: 45.63vh;
    }
    .selection-5 .list_03 {
      left: 59.73vw;
      bottom: 45.63vh;
    }
    .selection-5 .list_04 {
      left: 70.13vw;
      bottom: 20.68vh;
    }

    /*selection-6*/
    .selection-6 {
      height: 103.15vh;
      background: url('../assets/011.jpg') center center no-repeat;
      background-size: cover;
    }
    .selection-6 .discr-con {
      padding-top: 8.85vh;
    }
    
    #swiper02 {
      height: 73.67vh;
    }
    
    .selection-6 .list_div {
      display: block;
      width: 79.47vw;
      height: 53.97vh;
      margin: 0 auto;
    }
    .selection-6 .list_div img {
      width: 100%;
      height: 100%;
    }
    .selection-6 .list_div p {
      line-height: 17.33vw;
      font-size: 5.87vw;
      background: #fff;
    }
     
    
    /*selection-7*/
    .selection-7 {
      height: 100vh;
    }
    .selection-7 .discr-con {
      padding-top: 13.34vh;
    }
    
    .selection-7 .cont {
      text-align: center;
      padding-top: 7.05vh;
    }
    .selection-7 .list_div {
      display: inline-block;
      width: 32vw;
      height: 32vw;
      margin: 0 5.47vw 4.8vh 5.47vw;
    }
    .selection-7 .list_div:nth-child(1) {
      -webkit-animation: scale 1.6s infinite;
      animation: scale 1.6s infinite;
    }
    .selection-7 .list_div:nth-child(2) {
      -webkit-animation: scale 1.6s infinite;
      animation: scale 1.6s infinite;
      animation-delay: 2s;
    }
    .selection-7 .list_div:nth-child(3) {
      -webkit-animation: scale 1.6s infinite;
      animation: scale 1.6s infinite;
      animation-delay: 3s;
    }
    .selection-7 .list_div:nth-child(4) {
      -webkit-animation: scale 1.6s infinite;
      animation: scale 1.6s infinite;
      animation-delay: 4s;
    }
    .selection-7 .cont {
      display: block;
    }

    .selection-7 .list_div img {
      display: block;
      width: 10.67vw;
      margin: 0 auto 1.57vh;
    }
    .selection-7 .list_div p {
      font-size: 3.73vw;
    }
    .selection-7 .list_div_con {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100%;
    }
    .selection-7 .sel-con {
      height: 100%;
      background: url('../assets/012.jpg') center center no-repeat;
      background-size: cover;
    }

    /*向下效果*/
    @-webkit-keyframes fall {
      0% {
        -webkit-transform: translateY(-20px);
        -moz-transform: translateY(-20px);
        -ms-transform: translateY(-20px);
        -o-transform: translateY(-20px);
      }
      60% {
        -webkit-transform: translateY(15px);
        -moz-transform: translateY(15px);
        -ms-transform: translateY(15px);
        -o-transform: translateY(15px);
      }
      100% {
        -webkit-transform: translateY(65px);
        -moz-transform: translateY(65px);
        -ms-transform: translateY(65px);
        -o-transform: translateY(65px);
      }
    }
    @keyframes fall {
      0% {
        -webkit-transform: translateY(-20px);
        -moz-transform: translateY(-20px);
        -ms-transform: translateY(-20px);
        -o-transform: translateY(-20px);
      }
      60% {
        -webkit-transform: translateY(15px);
        -moz-transform: translateY(15px);
        -ms-transform: translateY(15px);
        -o-transform: translateY(15px);
      }
      100% {
        -webkit-transform: translateY(65px);
        -moz-transform: translateY(65px);
        -ms-transform: translateY(65px);
        -o-transform: translateY(65px);
      }
    }
    @-webkit-keyframes scale {
      0% {
        -webkit-transform: scale(1);
        -moz-transform: scale(1);
        -ms-transform: scale(1);
        -o-transform: scale(1);
        transform: scale(1);
      }
      60% {
        -webkit-transform: scale(1.15);
        -moz-transform: scale(1.15);
        -ms-transform: scale(1.15);
        -o-transform: scale(1.15);
        transform: scale(1.15);
      }
      100% {
        -webkit-transform: scale(1);
        -moz-transform: scale(1);
        -ms-transform: scale(1);
        -o-transform: scale(1);
        transform: scale(1);
      }
    }

    @keyframes scale {
      0% {
        -webkit-transform: scale(1);
        -moz-transform: scale(1);
        -ms-transform: scale(1);
        -o-transform: scale(1);
        transform: scale(1);
      }
      60% {
        -webkit-transform: scale(1.15);
        -moz-transform: scale(1.15);
        -ms-transform: scale(1.15);
        -o-transform: scale(1.15);
        transform: scale(1.15);
      }
      100% {
        -webkit-transform: scale(1);
        -moz-transform: scale(1);
        -ms-transform: scale(1);
        -o-transform: scale(1);
        transform: scale(1);
      }
    }
  }
  
  @media screen and (min-width: 751px) {
    .selection-6 .list_div:hover {
      box-shadow: 0 4px 43px 0 rgba(0, 0, 0, 0.40);
      -webkit-transform: scale(1.15);
      transform: scale(1.15);
      -webkit-transition: all 0.8s;
      transition: all 0.8s;
    }
  }
</style>
