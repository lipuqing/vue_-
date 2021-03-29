<template>
  <div class="banner-wrap">
    <div class="wrapper">
      <swiper :options="swiperOptions" v-if="list.length">
        <swiper-slide v-for="item in list" :key="item.id">
          <div class="imgwrapepr">
            <div class="banner-info">
              <h1>{{ item.title }}</h1>
              <!-- <p>{{$t('lang.slide1p')}}</p> -->
            </div>
            <img class="bannerimg" :src="item.src" />
          </div>
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
// swiper options example:
import axios from "axios";
import url from "../../../modules/api.js";
export default {
  name: "HomeSwiper",
  data() {
    return {
      swiperOptions: {
        loop: true,
        pagination: ".swiper-pagination",
        autoplay: 4000,
      },
      list: [
        {
          id: 0,
          src: "https://img.singschool.cn/wl/file/20210329120947347-1624175839.png",
          title: " ",
        },
        {
          id: 1,
          src: "https://img.singschool.cn/wl/file/20210329121339428-1032639369.png",
          title: " ",
        },
        {
          id: 2,
          src: "https://img.singschool.cn/wl/file/20210329121152809-107441631.png",
          title: " ",
        },
        {
          id: 3,
          src: "https://img.singschool.cn/wl/file/20210329152218805-1426597995.png",
          title: " ",
        },
        {
          id: 4,
          src: "https://img.singschool.cn/wl/file/20210329121128761-1682888250.png",
          title: " ",
        },
      ],
    };
  },
  mounted() {
    // axios.get(url.swiperLists).then(res => {
    //   this.list = res.data.data.data
    // })
  },
};
</script>
<style scoped>
.banner-wrap {
  display: flex;
  justify-content: center;
  width: 100%;
  height: 734px;
  overflow: hidden;
  position: relative;
}
.wrapper {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  z-index: 0;
}
.imgwrapepr {
  height: 884px;
  width: 100%;
  margin: 0 auto;
  position: relative;
}
.bannerimg {
  /* width: 100%; */
  height: 100%;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
.banner-info {
  position: absolute;
  top: 300px;
  left: 50%;
  transform: translateX(-50%);
}
.banner-info h1 {
  color: #fff;
  font-size: 50px;
  font-weight: 300;
  line-height: 50px;
  margin-bottom: 25px;
}
.banner-info p {
  color: #fff;
  font-size: 17px;
  font-weight: 400;
}
.wrapper >>> .swiper-pagination {
  position: absolute;
  bottom: 180px;
}
@media screen and (max-width: 767px) {
  .banner-info h1 {
    width: 100%;
    word-break: keep-all;
    word-break: normal;
    padding-right: 30px;
  }
  .banner-info {
    width: 60%;
    word-wrap: break-word;
    word-break: normal;
    text-align: center;
    margin-left: 5%;
    padding-right: 5%;
    position: absolute;
    top: 300px;
  }
}
@media screen and (max-width: 496px) {
  .banner-wrap {
    height: 586px;
  }
  .banner-info {
    top: 260px;
  }
  .swiper-pagination {
    bottom: 340px !important;
  }
  .banner-info h1 {
    font-size: 30px;
    line-height: 38px;
    word-break: keep-all;
  }
}
</style>
