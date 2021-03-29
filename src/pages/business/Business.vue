<template>
  <div>
    <Home-Nav :navindex="1"></Home-Nav>
    <Home-Banner :list="list"></Home-Banner>
    <Business-Item :businessList="businessList"></Business-Item>
    <Home-Footer></Home-Footer>
  </div>
</template>

<script>
import HomeNav from "../common/Nav";
import HomeBanner from "../common/Banner";
import BusinessItem from "../common/BussinessItem";
import HomeFooter from "../common/Footer";
import axios from "axios";
import url from "../../modules/api.js";
export default {
  name: "Bussiness",
  components: {
    HomeNav,
    HomeFooter,
    HomeBanner,
    BusinessItem,
  },
  data() {
    return {
      list: [
        {
          id: 1,
          h2: "业务&服务",
          p: "我们从企业业务实际出发，提出富有前瞻性的解决方案，并将策略和执行结合起来。",
        },
      ],
      businessList: [
        {
          id: 0,
          h2: "好声音大礼包",
          p: "我们从学员实际角度出发，提出富有前瞻性的解决方案，并将策略和执行结合起来。",
          p2: " ",
          p3: " ",
          url: "https://img.singschool.cn/wl/file/20210329150732071-2033630309.png",
        },
        {
          id: 1,
          h2: "历届学员纪念大碟",
          p: "我们从企业业务实际出发，提出富有前瞻性的解决方案，并将策略和执行结合起来。",
          p2: "",
          p3: "",
          url: "https://img.singschool.cn/wl/file/20210329150911204-684540414.png",
        },
        {
          id: 2,
          h2: "好声音第一课",
          p: "我们从企业业务实际出发，提出富有前瞻性的解决方案，并将策略和执行结合起来。",
          p2: "",
          p3: "",
          url: "https://img.singschool.cn/wl/file/20210329150927594-1407563244.png",
        },
        {
          id: 3,
          h2: "星声教唱VIP",
          p: "我们从企业业务实际出发，提出富有前瞻性的解决方案，并将策略和执行结合起来。",
          p2: "",
          p3: "",
          url: "https://img.singschool.cn/wl/file/20210329150956170-1007469152.png",
        },
        {
          id: 4,
          h2: "好声音话筒",
          p: "我们从企业业务实际出发，提出富有前瞻性的解决方案，并将策略和执行结合起来。",
          p2: "",
          p3: "",
          url: "https://img.singschool.cn/wl/file/20210329151014442-1647058438.png",
        },
        {
          id: 5,
          h2: "好声音导师纪念徽章",
          p: "我们从企业业务实际出发，提出富有前瞻性的解决方案，并将策略和执行结合起来。",
          p2: "",
          p3: "",
          url: "https://img.singschool.cn/wl/file/20210329151032738-1675369283.png",
        },
      ],
    };
  },
  mounted() {
    // axios.get(url.producDetailtList).then((res) => {
    //   this.businessList = res.data.list;
    // });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
