<template>
  <div class="container">
    <h2 class="text-center">合作伙伴</h2>
    <p class="text-center">很荣幸，能与众多行业精英共同成长</p>
    <div class="row">
      <div class="item" v-for="item in list" :key="item.id">
        <!-- <img class="w-100" style="display:none" :src="item.url" />
        <p class="click" style=" cursor:pointer;" @click="showImg(item.id)">{{ item.text }}</p> -->
      </div>
    </div>
    <!-- <div class="paybox" v-if="clickType >= 0" @click="showImg(-1)">
      <div class="box">
        <img
          class="imgs"
          src="https://img.singschool.cn/wl/file/20210329171635458-280454198.png"
          alt=""
        />
      </div>
    </div> -->
  </div>
</template>
<script>
import axios from "axios";
import url from "../../../modules/api.js";
export default {
  name: "Partner",
  data() {
    return {
      list: [
        {
          id: "0",
          text: "好声音大礼包",
        },
        {
          id: "1",
          text: "历届学员纪念大碟",
        },
        {
          id: "2",
          text: "好声音第一课",
        },
        {
          id: "3",
          text: "星声教唱VIP",
        },
        {
          id: "4",
          text: "好声音话筒",
        },
        {
          id: "5",
          text: "好声音导师纪念徽章",
        },
      ],
      clickType: -1,
    };
  },
  mounted() {
    // axios.get(url.partnerList).then((res) => {
    //   this.list = res.data.list;
    // });
  },
  methods: {
    showImg(e) {
      console.log(e);
      this.clickType = e;
    },
  },
};
</script>
<style scoped>
.container {
  margin-top: 50px;
  background: #ffffff;
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
.box {
  width: 200px;
  height: 200px;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.container h2 {
  font-weight: 500;
  font-size: 40px;
  padding-top: 30px;
  padding-bottom: 10px;
}
.click:hover {
  color: blueviolet;
}
.text-center {
  text-align: center;
  margin-bottom: 10px;
}
.row {
  width: 1175px;
  padding-top: 10px;
  margin: 0 auto;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  justify-content: space-around;
  /* flex-direction: column; */
  padding-bottom: 40px;
}
/* img {
  width: 170px;
  height: 84.2px;
  padding: 0 10px 0 0;
} */
@media screen and (max-width: 1175px) {
  .row {
    max-width: 70%;
  }
  .item {
    width: 28.66667%;
    margin-bottom: 10px;
    /* width: 16.66667%; */
  }
  /* img {
    width: 80px;
    height: 47.36px;
  } */
  .box .img {
    width: 100% !important;
  }
}
@media screen and (max-width: 767px) {
  .row {
    max-width: 70%;
    flex-direction: column;
    margin: 0 auto;
  }
  .item {
    /* width: 33.33333%; */

    width: 100%;
    text-align: center;
    line-height: 25px;
  }
  /* img {
    width: 160px !important;
    height: 84.2px !important;
  } */
  .box .img {
    width: 100% !important;
  }
}
@media screen and (max-width: 496px) {
  .row {
    max-width: 70%;
  }
  .item {
    width: 100%;
    text-align: center;
    line-height: 25px;
  }
  /* img {
    width: 80px !important;
    height: 47.36px !important;
  } */
  .box .img {
    width: 100% !important;
  }
}
</style>
