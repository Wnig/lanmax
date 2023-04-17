<template>
  <header>
    <div class="pc">
      <div class="cons" v-if="!show">
        <div class="header clearfix">
          <a class="logo" @click="jump">
            <img src="../assets/1.svg" alt="">
          </a>
          <img id="js-hamburger" @click="isShow" class="nav_btn" src="../assets/5.svg" alt="">
        </div>
      </div>
      <transition name="fade" enter-active-class="fadeInDown" leave-active-class="fadeOutUp">
        <div class="header_" :class="{open: show}" v-if="show">
          <div class="cons">
            <div class="header clearfix">
              <a class="logo" @click="jump">
                <img src="../assets/2.svg" alt="">
              </a>
              <img @click="isShow" class="nav_btn" src="../assets/6.svg" alt="">
            </div>      
            <nav v-if="show">
              <ul>
                <li v-for="(navs, index) in navData" v-bind:class="{'btn_sel': index == num}" @click="selMenus(index)">
                  <router-link :to="navs.links">{{navs.tit}}</router-link>
                </li>
                <li>
                  <a href="http://abc.smartmapdt.com/lmm/home">后台登录</a>
                </li>
              </ul>
            </nav>
          </div>
        </div>
        <!-- <svg class="shape-overlays" id="js-shape-overlays" viewBox="0 0 100 100" preserveAspectRatio="none">
          <path class="shape-overlays__path" d="M 0 100 C 16.666666666666664 100 16.666666666666664 100 33.33333333333333 100 C 49.99999999999999 100 49.99999999999999 100 66.66666666666666 100 C 83.33333333333334 100 83.33333333333334 100 100 100 V 100 H 0"></path>
          <path class="shape-overlays__path" d="M 0 100 C 16.666666666666664 100 16.666666666666664 100 33.33333333333333 100 C 49.99999999999999 100 49.99999999999999 100 66.66666666666666 100 C 83.33333333333334 100 83.33333333333334 100 100 100 V 100 H 0"></path>
          <path class="shape-overlays__path" d="M 0 100 C 16.666666666666664 100 16.666666666666664 100 33.33333333333333 100 C 49.99999999999999 100 49.99999999999999 100 66.66666666666666 100 C 83.33333333333334 100 83.33333333333334 100 100 100 V 100 H 0"></path>
          <path class="shape-overlays__path" d="M 0 100 C 16.666666666666664 100 16.666666666666664 100 33.33333333333333 100 C 49.99999999999999 100 49.99999999999999 100 66.66666666666666 100 C 83.33333333333334 100 83.33333333333334 100 100 100 V 100 H 0"></path>
        </svg> -->
      </transition>
    </div>
    <div class="mob">
      <div class="cons">
        <div class="header clearfix">
          <a class="logo" @click="jump">
            <img src="../assets/001.svg" alt="">
          </a>
          <img class="nav_btn" @click="isShow" src="../assets/002.svg" alt="">
        </div>
      </div>
      <div class="nav-con" v-if="show" @click="isShow">
        <nav>
          <ul>
            <li v-for="(navs, index) in navData" v-bind:class="{'btn_sel': index == num}" @click="selMenus(index)">
              <router-link :to="navs.links">{{navs.tit}}</router-link>
            </li>
            <li>
              <a href="http://abc.smartmapdt.com/lmm/home">后台登录</a>
            </li>
          </ul>
          <div class="hot">
            <p>全国统一客户热线：</p>
            <h2>400-666-7113</h2>
          </div>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
import '../../static/js/flow.js'
let storage = window.sessionStorage;
export default {
  name: 'Header',
  data() {
    return {
      navData: [
        {tit: '首页', links:'/'},
        {tit: '解决方案', links:'/Solution'},
        {tit: '招商联盟', links:'/Join'},
        {tit: '关于我们', links:'/About'},
      ],
      num: '',
      show: false
    }
  },
  created: function() {
    if(storage['selNums']) {
      this.num= storage['selNums'];
    } else {
      this.num = 0;
    };
  },
  methods: {
    selMenus(index) {
      storage['selNums'] = index;
      this.selShow = false;
    },
    isShow() {
      //点击：左侧菜单栏 收起-展开
      this.show = ! this.show;
    },
    jump() {
      storage['selNums'] = 0;
      this.selShow = false;
      this.$router.push({path: '/'});
    }
  },
  mounted() {
  },
  components: {

  }
}
</script>

<style scoped>
  /*svg*/
  :root {
    --path-fill-4: #15203f;
    --path-fill-3: #1f2d54;
    --path-fill-2: #456085;
    --path-fill-1: #d5e2ea;
  }
  .shape-overlays {
    pointer-events: none;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 85;
    width: 100%;
    height: 100vh;
  }

  .shape-overlays.is-opened {
    pointer-events: auto;
  }

  .shape-overlays__path:nth-of-type(1) {
    fill: var(--path-fill-1);
  }

  .shape-overlays__path:nth-of-type(2) {
    fill: var(--path-fill-2);
  }

  .shape-overlays__path:nth-of-type(3) {
    fill: var(--path-fill-3);
  }

  .shape-overlays__path:nth-of-type(4) {
    fill: var(--path-fill-4);
  }


  header {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    z-index: 999999999999;
  }
  .header_ {
    overflow: hidden;
  }

  @-webkit-keyframes fadeInDown {
    0% {
      width: 0;
      height: 0;
      opacity: 0;
      -webkit-transform: translate3d(0, -100%, 0);
      transform: translate3d(0, -100%, 0);
    }
    100% {
      width: 100%;
      height: 100vh;
      opacity: 1;
      -webkit-transform: translate3d(0, -20%, 0);
      transform: translate3d(0, -20%, 0);
    }
  }

  @keyframes fadeInDown {
    0% {
      height: 0;
      opacity: 0;
      -webkit-transform: translate3d(0, 0%, 0);
      transform: translate3d(0, 0%, 0);
    }
    100% {
      height: 100vh;
      opacity: 1;
      -webkit-transform: translate3d(0, 0%, 0);
      transform: translate3d(0, 0%, 0);
    }
  }

  .fadeInDown {
    -webkit-animation: fadeInDown 0.8s ease-in-out;
    animation: fadeInDown 0.8s ease-in-out;
  }

  .cons {
    width: 84.67vw;
    padding-top: 5.37vh;
    margin: 0 auto;
  }
  .open {
    background-color: #fff;
  }
  .logo {
    float: left;
    width: 15.83vw;
    cursor: pointer;
  }
  .logo img {
    display: block;
    width: 100%;
  }
  .nav_btn {
    float: right;
    width: 3.13vw;
    padding-top: 1.57vh;
    cursor: pointer;
  }

  nav {
    height: 77.13vh;
    padding-top: 7.41vh;
    padding-left: 26.72vw;
  }
  nav ul {

  }
  nav li {
    margin-bottom: 6.76vh;
  }
  nav li a {
    display: block;
    color: #000;
    font-size: 1.82vw;
  }
  nav li.btn_sel a {
    color: #58B2FF;
  }
  nav li.btn_sel {
    position: relative;
  }
  nav li.btn_sel:after {
    content: '';
    position: absolute;
    left: 0;
    bottom: -0.94vw;
    width: 100%;
    height: 0.31vw;
    font-size: 2vw;
    background: url('../assets/3.svg') left center no-repeat;
    background-size: auto 100%;
  }

  @media screen and (max-width: 750px) {
    .logo {
      width: 42.93vw;
    }
    .nav_btn {
      width: 9.6vw;
      height: 9.6vw;
    }
    .cons {
      width: 84.67vw;
      padding-top: 2.55vh;
      padding-bottom: 5.1vh;
      margin: 0 auto;
    }
    .mob {
      /*position: fixed;
      left: 0;
      top: 0;*/
      width: 100%;
      background: url('../assets/path02.png') center center no-repeat;
      background-size: 100% 100%; 
      z-index: 99999999999999999;
    }
    .nav-con {
      position: fixed;
      left: 0;
      top: 0;
      width: 100%;
      height: 100vh;
      background: rgba(0, 0, 0, 0.65);
      z-index: 999999999999999999;
    }
    nav {
      width: 56.53vw;
      height: 78.11vh;
      padding: 13.94vh 0 7.95vh 11.2vw;
      background: #FFFFFF;
      box-shadow: 0 7px 10px 0 rgba(0, 0, 0, 0.44);
    }
    nav li a {
      font-size: 4.8vw;
    }
    nav li.btn_sel:after {
        position: absolute;
        left: 0;
        bottom: -0.94vw;
        height: 0.45vw;
    }
    nav p {
      margin-bottom: 1.05vh;
      color: #797979;
      font-size: 3.2vw;
    }
    nav h2 {
      color: #000000;
      line-height: 6.67vw;
      font-size: 6.67vw;
      font-weight: 600;
    }
    nav .hot {
      position: absolute;
      left: 11.2vw;
      bottom: 7.95vh;
    }
  }
</style>
