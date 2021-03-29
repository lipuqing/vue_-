<template>
  <div style="padding-bottom:5vh">
    <div class="container" v-for="item in businessList" :key="item.id"  @click="showImg(item.id)">
      <div class="main clear"  style=" cursor:pointer;">
        <div class="main-inner">
          <h2>
            <strong>{{item.h2}}</strong>
          </h2>
          <p class="text-muted">{{item.p}}</p>
          <hr />
          <p>{{item.p2}}</p>
          <p>{{item.p3}}</p>
          <!-- <h3>服务特点</h3>
          <ul class="pl-3">
            <li v-for="(li,index) in item.li" :key="index">{{li}}</li>
          </ul>-->
          <button class="btn"  style=" cursor:pointer;">  点击扫码购买 </button>
        </div>
        <div class="box">
          <img :src="item.url" alt srcset />
        </div>

      </div>
      
    <div class="paybox" v-if="clickType >= 0" @click.stop="showImg(-1)">
      <div class="box_sa">
        <img
          class="imgs"
          src="https://img.singschool.cn/wl/file/20210329171635458-280454198.png"
          alt=""
        />
      </div>
    </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Banner',
  data(){
    return{
      clickType:-1,
    }
  },
  props: {
    businessList: Array
  },
  methods: {
    showImg(e) {
      console.log(e);
      this.clickType = e;
    },
  },
}
</script>
<style scoped>
.clear::after {
  display: block;
  clear: both;
  content: "";
}
.container {
  overflow: hidden;
}
.btn{
  padding: 5px 10px;
  border-radius: 500px;
  margin-bottom: 10px;
  background: rgba(0, 0, 255, 0.466);
  color: #fff;
}
.paybox {
  position: fixed;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.2);
  z-index: 99;
}
.box_sa {
  width: 200px;
  height: 200px;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.box_sa img{
  width: 100%;
}
.main {
  margin-top: 80px;
  position: relative;
  margin-left: 30px;
}
.main-inner {
  background: #fff;
  padding: 0 40px;
  float: left;
  max-width: 50%;
  position: absolute;
  right: 690px;
  box-shadow: 0 10px 10px rgba(0, 0, 0, 0.15) !important;
}
@media screen and (max-width: 1360px) {
  .main-inner {
    right: 600px;
  }
  .box {
    margin-right: 0 !important;
  }
}
@media screen and (max-width: 1200px) {
  .main-inner {
    right: 20%;
  }
  .box {
    opacity: 0;
  }
}
@media screen and (max-width: 756px) {
  .main {
    padding: 0 10%;
    height: 584px;
    margin-top: 20px;
    margin-bottom: -15px;
  }
  .main-inner {
    max-width: 90% !important;
    right: 10%;
  }
  .box {
    display: none;
  }
}
@media screen and (max-width: 496px) {
  .main {
    padding: 0 10%;
    /* height: 584px; */
    height: 310px;
    margin-top: 20px;
    margin-bottom: -15px;
  }
  .main-inner {
    max-width: 90% !important;
    right: 10%;
  }
}
.main h2 {
  font-size: 36px;
  font-weight: bolder;
  margin-top: 0.83rem;
  margin-bottom: 0.83rem;
}
.main h3 {
  font-size: 30px;
  margin-block-start: 0.83em;
  margin-block-end: 0.83em;
}
.main ul {
  margin-left: 15px;
}
.main li {
  list-style-type: disc;
  margin-block-start: 0.83em;
  margin-block-end: 0.83em;
}
.main p {
  font-size: 16px;
  font-weight: 400;
  line-height: 1.5;
  color: #212529;
  text-align: left;
  margin-top: 0;
  margin-bottom: 20px;
}
.box {
  width: 350px;
  height: 350px;
  float: right;
  margin-right: 20%;
  margin-top: -10px;
}
.box img {
  width: 350px;
  height: 350px;
}
</style>
