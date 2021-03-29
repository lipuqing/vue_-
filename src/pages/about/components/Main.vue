<template>
  <div class="container"  style="padding-bottom:5vh">
    <div class="main clear">
      <div class="main-inner">
        <h2>
          <strong>灿星文化传媒股份有限公司</strong>
        </h2>
        <p class="text-muted">
          上海灿星文化传媒股份有限公司（以下简称“灿星文化”、“公司”）是国内领先的电视和互联网节目制作和运营商。公司注册在上海市长宁区，注册资本金3.6亿元人民币。
        </p>
        <hr />
        <p>
          <strong>
            公司已在文化综艺节目领域形成了工业化、一体化的制作运营体系，建立了从节目研发、遴选，到节目内容制作落地，再到节目推广营销及后续衍生品开发运营的完整业务流程，形成了一批引领国内娱乐文化发展方向的“大投入、大制作”现象级电视节目，在收获高收视的同时也取得良好的社会反响。</strong
          >
          公司制作的文化综艺节目超过20档，内容涵盖音乐、舞蹈、综合才艺、访谈等多种类型。其中不乏《中国好声音》、《中国新歌声》、《出彩中国人》、《中国好歌曲》、《了不起的挑战》、《蒙面唱将猜猜猜》等具有一定社会影响力的节目。经过多年的深耕细作，公司已经获得了观众和业内人士的一致认可，“灿星制作”已成为传媒界知名的品牌标志，建立了业内颇具影响力的娱乐资源整合平台，成为合作伙伴和观众可信赖的娱乐品牌。在商业模式创新方面，公司与电视台“联合制作，共同运营”的新型商业模式，对行业长远健康发展产生了深远影响。
          <br />　　
        </p>
      </div>
      <div class="box">
        <img src="https://img.singschool.cn/wl/file/20210329145127212-1529994322.jpg?imageView2/0/w/450/h/490" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Banner",
};
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
    height: 600px;
  }
  .main-inner {
    max-width: 90% !important;
    right: 5%;
  }
  .box {
    display: none;
  }
}

.main h2 {
  font-size: 36px;
  font-weight: bolder;
  /* margin-block-start: 0.83em;
  margin-block-end: 0.83em; */
  margin-top: 0.83rem;
  margin-bottom: 0.83rem;
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
  width: 450px;
  height: 490px;
  float: right;
  margin-right: 20%;
  margin-top: -20px;
}
.box img {
  width: 450px;
  height: 490px;
}
@media screen and (max-width: 496px) {
  .main {
    margin-top: 30px;
    padding: 10%;
    height: 700px;
  }
  .main-inner {
    max-width: 90% !important;
    right: 10%;
  }
}
</style>
