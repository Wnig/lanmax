<template>
  <footer class="footer">
    <div class="pc">
      <div class="left">
        <p>宁波日朗轻工电器制造有限公司<br/>Ningbo rilang light electrical appliances manufacturing Co,. Ltd. </p>
        <p>总部地址：中国浙江省余姚市陆埠镇五马开发区<br/>Add:Wuma Area for development Lubu Town Yuyao Zhejiang China.</p>
      </div>
      <div class="bor"></div>
      <div class="right">
        <div class="right-con">
          <p>全国统一客户热线</p>
          <h2>400-666-7113</h2>
        </div>
        <img class="code" src="../assets/34.jpg" alt="">
      </div>
    </div>
    <div class="mob">
      <div class="cont">
      <div class="conts">
        <img class="code" src="../assets/34.jpg" alt="">
        <p class="comp">宁波日朗轻工电器制造有限公司<br/>Ningbo rilang light electrical<br/> appliances manufacturing Co,. Ltd. </p>
        <p class="addr">总部地址：中国浙江省余姚市陆埠镇五马开发区<br/>Add:Wuma Area for development Lubu Town<br/> Yuyao Zhejiang China.</p>
        <p class="comp">全国统一客户热线</p>
        <h2 class="hot">400-666-7113</h2>
      </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  components: {
  }
}
</script>

<style scoped>
  footer {
    color: #797979;
    background: #232526;
  }
  footer .pc {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 21.3vh;
  }
  .left {
    margin-right: 3.28vw;
    font-size: 1.04vw;
  }
  .left p {
    margin-bottom: 0.94vh;
  }
  .bor {
    width: 0.1vw;
    height: 12.41vh;
    margin-right: 3.8vw;
    background: #575757;
  }
  .right {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .right-con {
    float: left;
    margin-right: 2.5vw;
  }
  .right p {
    margin-bottom: 0.73vh;
    font-size: 1.04vw;
  }
  .right h2 {
    font-size: 2.6vw;
    font-weight: 600;
  }
  .right .code {
    float: right;
    width: 7.08vw;
  }
  .mob {
    display: none;
  }
  @media screen and (max-width: 750px) {
    footer .pc {
      display: none;
    }
    .mob {
      display: block;
      height: 83.66vh;
    }
    .cont {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100%;
    }
    .conts {
    }
    .cont img {
      display: block;
      width: 32.8vw;
      margin: 0 auto 5.25vh;
    }
    .cont .comp {
      margin-bottom: 2.55vh;
      color: #797979;
      text-align: center;
      font-size: 3.73vw;
    }
    .cont .addr {
      margin-bottom: 3.9vh;
      color: #4D4D4D;
      text-align: center;
      font-size: 3.73vw;
    }
    .cont .hot {
      color: #797979;
      text-align: center;
      line-height: 8vw;
      font-size: 8vw;
      font-weight: 600;
    }
  }
</style>
