<template>
  <div id="app" style="float:left">
    <el-container>
      <el-header>
        <el-row>
          <el-col :span="24">
            <div>
              <el-row>
                <el-col :span="14">
                  <div>
                    <h1>产线机台现场监控</h1>
                  </div>
                </el-col>
                <el-col :span="10">
                  <div style="float:right">
                    <h3>2020-04-09 13:19:55</h3>
                  </div>
                </el-col>
              </el-row>
            </div>
          </el-col>
        </el-row>
      </el-header>
      <el-main>
        <PartTop/>
        <PartMain/>
        <PartFooter/>
      </el-main>
    </el-container>
  </div>
</template>

<script>

import PartTop from "./components/PartTop";
import PartMain from "./components/PartMain";
import PartFooter from "./components/PartFooter";

export default {
  name: "App",
  components: {
    PartTop,
    PartMain,
    PartFooter,
  }
};
</script>

<style>
html {
  margin: 0;
  padding: 0;
}
body {
  margin: 0;
  padding: 0;
  height: 100%;
  background-color: rgba(5, 46, 79, 1);
}
.el-card{
  background-color: rgba(4, 33, 56, 0.5);
  border: none
}
h1,h3,h5{
  color: rgb(79, 217, 247);
}
.el-main {
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
#app {
  width: 100%;
}
</style>
