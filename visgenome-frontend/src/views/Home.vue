<template>
  <div class="home">
    <el-row class="visgenome">
      <img alt="home logo" src="../assets/home.png" />
      Welcome to iVisgenome
    </el-row>
    <!-- :style="{minHeight: minHeight + 'px'}" -->
    <el-row class="item">
      <div class="title">
        <img alt="genome logo" src="../assets/title.png" />
        Introduction
      </div>
      <div class="intro">
        <p>
          <b>iVisgenome</b> can be used to visualize the whole-genome (e.g.
          <b>Human, Mouse, and Yeast</b>) sequences represented by
          <i>k</i>-nucleotide physicochemical property values. We integrate
          <a href="http://circos.ca/" target="_blank">Circos</a> by circular
          ideogram layout , and
          <a href="https://www.jbrowse.org/jb2/" target="_blank">JBrowse 2</a>
          for visualizing the whole genome sequence by linear genome view. The
          following images are examples of embedded Circos and Jbrowse 2 for
          visualizing our biological sequence values.
        </p>
        <p>
          Users can also visualize other genomes by configuring files in the
          same format as these of Human, Mouse, and Yeast. The file format is
          explained on
          <a href="/help?id=dataFormat">Help->Data processing</a> section and
          all the source codes of iVisGenome can be downloaded from <a href="/download"
            >Download</a
          >
          page.
        </p>
        <p>
          This website is free and open to all users and there is no login requirement.
        </p>
        <el-row type="flex" justify="space-between" class="circosImg">
          <el-col :span="11">
            <el-row class="imageTitle">Circos</el-row>
            <!-- <el-row>
              <el-col class="item" :span="12">
                <a href="/vis_circos/human">
                  <img
                    alt="example"
                    src="../assets/home/ex02.png"
                    style="width: 100%; height: auto"
                  />
                </a>
              </el-col>
              <el-col class="item" :span="12">
                <a href="/vis_circos/mouse">
                  <img
                    alt="example"
                    src="../assets/home/ex03.png"
                    style="width: 100%; height: auto"
                  />
                </a>
              </el-col>
            </el-row> -->
            <el-row type="flex" justify="space-around" style="margin-top: 5%">
              <el-col class="item" :span="16">
                <a href="/vis_circos/human">
                  <img
                    alt="example"
                    src="../assets/home/circos.png"
                    style="width: 100%; height: auto"
                  />
                </a>
              </el-col>
            </el-row>
          </el-col>
          <el-col :span="11">
            <el-row class="imageTitle"> Tracks </el-row>
            <el-row type="flex" justify="space-around" style="margin-top: 10%">
              <a href="/genomes/yeast">
                <img
                  class="item"
                  alt="example"
                  src="../assets/home/tracks.png"
                  style="width: 100%; height: auto"
                />
              </a>
            </el-row>
          </el-col>
        </el-row>
        <el-divider>
          <i style="color: blue" class="el-icon-orange"></i>
        </el-divider>
      </div>
    </el-row>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  data() {
    return {};
  },
};
</script>

<style scoped>
.home {
  width: 100%;
  min-height: calc(100% - 120px);
  text-align: left;
}

.visgenome {
  width: 100%;
  height: 80px;
  line-height: 80px;
  text-align: center;
  font-size: 1.5em;
  /* border-bottom: 5px groove #a5c2a0; */
  background: #f5f5dc;
}

.visgenome img {
  width: 45px;
  height: auto;
  vertical-align: middle;
}

.title {
  height: 40px;
  line-height: 40px;
  font-size: 24px;
  padding: 30px 60px;
}

.title img {
  width: 40px;
  height: 40px;
  vertical-align: middle;
  margin-right: 10px;
}

.intro {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 18px;
  padding: 0 60px;
  text-align: justify;
  line-height: 1.5em;
}

.download {
  text-indent: 2em;
  margin: 5px;
}

a {
  font-style: italic;
  font-weight: bolder;
  color: #a5c2a0;
}

.imageTitle {
  width: 100%;
  height: 40px;
  line-height: 40px;
  text-align: center;
  background-color: #deeedc;
  border-radius: 10px;
}

/* 以下设置：图片在划过的时候放大 */
/* .circosImg {
  overflow: hidden;
} */
.circosImg .item {
  position: relative;
  transition: transform 1s;
}

.circosImg .item:hover {
  transform: scale(1.5);
  z-index: 1;
}
</style>
