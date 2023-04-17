<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  }
}
</script>

<style>
  /* CSS reset */
  html{color:#000;background:#fff;-webkit-tap-highlight-color:rgba(0,0,0,0);font-family: 'PingFangSC-Light',"Arial","Microsoft YaHei","微软雅黑","sans-serif";font-size: 12px;}
  body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,form,input,button,textarea,p,th,td,strong{padding:0;margin:0;font-family: 'PingFangSC-Light',"Arial","Microsoft YaHei","微软雅黑","sans-serif";}
  table{border-collapse:collapse;border-spacing:0;}
  img{border:0;}
  a{text-decoration:none; color:#999; outline:none;}/*此处待添加默认链接颜色*/
  var,em,strong{font-style:normal;}
  em,strong,th,var{font-style:inherit;font-weight:inherit;}
  li{list-style:none;}
  caption,th{text-align:left;}
  h1,h2,h3,h4{font-size:100%;font-weight:normal;}
  input,button,textarea,select,option{font-family:inherit; font-size:inherit;font-style:inherit;font-weight:inherit;}
  input,button,textarea,select{*font-size:100%;}
  .clearfix:after {content:"\200B"; display:block; height:0; clear:both; }
  .clearfix { *zoom:1; }
  
  video::-webkit-media-controls-enclosure {
    /*禁用播放器控制栏的样式*/
    display: none !important;
  }

  .blur {    
    -webkit-filter: blur(100vw); /* Chrome, Opera */
       -moz-filter: blur(100vw);
        -ms-filter: blur(100vw);    
            filter: blur(100vw);    
  }

  /*箭头*/
  .down-btn {
    overflow: hidden;
    position: absolute;
    left: 0;
    bottom: 15vh;
    width: 2.4vw;
    height: 2.4vw;
    border: 1px solid #fff;
    border-radius: 100%;
    outline: none;
    color: #fff;
    background: 0 0;
    z-index: 100;
    cursor: pointer;
  }
  .down-btn i {
    display: block;
    font-size: 1.35vw;
    -webkit-animation: fall .6s infinite;
    animation: fall .6s infinite;
  }

  .title {
    position: relative;
    margin-bottom: 4.91vh;
    color: #fff;
    text-align: center;
    font-size: 2.34vw;
  }
  .title:after {
    content: '';
    position: absolute;
    left: 0;
    bottom: -0.94vw;
    width: 100%;
    height: 0.31vw;
    font-size: 2vw;
    background: url('../src/assets/3.svg') center center no-repeat;
    background-size: auto 100%;
  }

  .discr {
    width: 75%;
    margin: 0 auto;
    color: #fff;
    text-align: center;
    font-size: 1.04vw;
  }

  /*向下效果*/
  @-webkit-keyframes fall {
    0% {
      -webkit-transform: translateY(-10px);
      -moz-transform: translateY(-10px);
      -ms-transform: translateY(-10px);
      -o-transform: translateY(-10px);
    }
    60% {
      -webkit-transform: translateY(15px);
      -moz-transform: translateY(15px);
      -ms-transform: translateY(15px);
      -o-transform: translateY(15px);
    }
    100% {
      -webkit-transform: translateY(45px);
      -moz-transform: translateY(45px);
      -ms-transform: translateY(45px);
      -o-transform: translateY(45px);
    }
  }
  @keyframes fall {
    0% {
      -webkit-transform: translateY(-10px);
      -moz-transform: translateY(-10px);
      -ms-transform: translateY(-10px);
      -o-transform: translateY(-10px);
    }
    60% {
      -webkit-transform: translateY(15px);
      -moz-transform: translateY(15px);
      -ms-transform: translateY(15px);
      -o-transform: translateY(15px);
    }
    100% {
      -webkit-transform: translateY(45px);
      -moz-transform: translateY(45px);
      -ms-transform: translateY(45px);
      -o-transform: translateY(45px);
    }
  }

  /*漂浮*/
  @-webkit-keyframes float_01 {
    0% {
      -webkit-transform: translateY(20px);
      -moz-transform: translateY(20px);
      -ms-transform: translateY(20px);
      -o-transform: translateY(20px);
    }
    50% {
      -webkit-transform: translateY(-20px);
      -moz-transform: translateY(-20px);
      -ms-transform: translateY(-20px);
      -o-transform: translateY(-20px);
    }
    100% {
      -webkit-transform: translateY(20px);
      -moz-transform: translateY(20px);
      -ms-transform: translateY(20px);
      -o-transform: translateY(20px);
    }
  }
  @keyframes float_01 {
    0% {
      -webkit-transform: translateY(20px);
      -moz-transform: translateY(20px);
      -ms-transform: translateY(20px);
      -o-transform: translateY(20px);
    }
    50% {
      -webkit-transform: translateY(-20px);
      -moz-transform: translateY(-20px);
      -ms-transform: translateY(-20px);
      -o-transform: translateY(-20px);
    }
    100% {
      -webkit-transform: translateY(20px);
      -moz-transform: translateY(20px);
      -ms-transform: translateY(20px);
      -o-transform: translateY(20px);
    }
  }
  @-webkit-keyframes float_02 {
    0% {
      -webkit-transform: translateY(30px);
      -moz-transform: translateY(30px);
      -ms-transform: translateY(30px);
      -o-transform: translateY(30px);
    }
    50% {
      -webkit-transform: translateY(-30px);
      -moz-transform: translateY(-30px);
      -ms-transform: translateY(-30px);
      -o-transform: translateY(-30px);
    }
    100% {
      -webkit-transform: translateY(30px);
      -moz-transform: translateY(30px);
      -ms-transform: translateY(30px);
      -o-transform: translateY(30px);
    }
  }
  @keyframes float_02 {
    0% {
      -webkit-transform: translateY(30px);
      -moz-transform: translateY(30px);
      -ms-transform: translateY(30px);
      -o-transform: translateY(30px);
    }
    50% {
      -webkit-transform: translateY(-30px);
      -moz-transform: translateY(-30px);
      -ms-transform: translateY(-30px);
      -o-transform: translateY(-30px);
    }
    100% {
      -webkit-transform: translateY(30px);
      -moz-transform: translateY(30px);
      -ms-transform: translateY(30px);
      -o-transform: translateY(30px);
    }
  }
  @-webkit-keyframes float_03 {
    0% {
      -webkit-transform: translateY(40px);
      -moz-transform: translateY(40px);
      -ms-transform: translateY(40px);
      -o-transform: translateY(40px);
    }
    50% {
      -webkit-transform: translateY(-40px);
      -moz-transform: translateY(-40px);
      -ms-transform: translateY(-40px);
      -o-transform: translateY(-40px);
    }
    100% {
      -webkit-transform: translateY(40px);
      -moz-transform: translateY(40px);
      -ms-transform: translateY(40px);
      -o-transform: translateY(40px);
    }
  }
  @keyframes float_03 {
    0% {
      -webkit-transform: translateY(40px);
      -moz-transform: translateY(40px);
      -ms-transform: translateY(40px);
      -o-transform: translateY(40px);
    }
    50% {
      -webkit-transform: translateY(-40px);
      -moz-transform: translateY(-40px);
      -ms-transform: translateY(-40px);
      -o-transform: translateY(-40px);
    }
    100% {
      -webkit-transform: translateY(40px);
      -moz-transform: translateY(40px);
      -ms-transform: translateY(40px);
      -o-transform: translateY(40px);
    }
  }
  @-webkit-keyframes float_04 {
    0% {
      -webkit-transform: translateY(15px);
      -moz-transform: translateY(15px);
      -ms-transform: translateY(15px);
      -o-transform: translateY(15px);
    }
    50% {
      -webkit-transform: translateY(-15px);
      -moz-transform: translateY(-15px);
      -ms-transform: translateY(-15px);
      -o-transform: translateY(-15px);
    }
    100% {
      -webkit-transform: translateY(15px);
      -moz-transform: translateY(15px);
      -ms-transform: translateY(15px);
      -o-transform: translateY(15px);
    }
  }
  @keyframes float_04 {
    0% {
      -webkit-transform: translateY(15px);
      -moz-transform: translateY(15px);
      -ms-transform: translateY(15px);
      -o-transform: translateY(15px);
    }
    50% {
      -webkit-transform: translateY(-15px);
      -moz-transform: translateY(-15px);
      -ms-transform: translateY(-15px);
      -o-transform: translateY(-15px);
    }
    100% {
      -webkit-transform: translateY(15px);
      -moz-transform: translateY(15px);
      -ms-transform: translateY(15px);
      -o-transform: translateY(15px);
    }
  }
  

  .mob {
    display: none;
  }
  @media screen and (max-width: 750px) {
    .pc {
      display: none;
    }
    .mob {
      display: block;
    }
    .selection {
      width: 100%;
      height: auto;
    }
    .title {
      margin-bottom: 7.5vh;
      font-size: 7vw;
    }
    .title:after {
      bottom: -4vw;
      height: 0.8vw;
      font-size: 2vw;
    }
    .discr {
      width: 75%;
      text-align: center;
      font-size: 3.73vw;
    }
    .down-btn {
      left: 50%;
      margin-left: -4.67vw;
      bottom: 4.65vh;
      width: 9.24vw;
      height: 9.24vw;
    }
    .down-btn i {
      display: block;
      font-size: 5.4vw;
    }

    #swiper .swiper-pagination-bullet-active {
      opacity: 1;
      background: #58B2FF;
    }

    #swiper02 .swiper-pagination-bullet {
      width: 8px;
      height: 8px;
      display: inline-block;
      border-radius: 100%;
      background: rgb(230, 243, 255);
      opacity: .2;
    }
    #swiper02 .swiper-pagination-bullet-active {
      opacity: 1;
      background: rgb(87, 176, 252);
    }
    
    .swiper-container-free-mode > .swiper-wrapper {
      -webkit-transition-timing-function: linear;    /*之前是ease-out*/
      -moz-transition-timing-function: linear;
      -ms-transition-timing-function: linear;
      -o-transition-timing-function: linear;
      transition-timing-function: linear;
      margin: 0 auto;
    }
  }
  @media screen and (min-width: 751px) {
    .selection {
      width: 100%;
      height: 100vh;
      overflow: hidden;
    }
  }
</style>
