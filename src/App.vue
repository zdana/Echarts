<template>
  <div id="app" style="float:left">
    <!-- <div id="title" style="height:100px;line-height:50px">
      <el-header>
        <el-row>
          <el-col :span="24">
            <div class="grid-content bg-purple-dark">
              <el-row>
                <el-col :span="14">
                  <div class="grid-content bg-purple">
                    <h1>产线机台现场监控</h1>
                  </div>
                </el-col>
                <el-col :span="10">
                  <div class="grid-content bg-purple-light">
                    <h3>2020-04-09 13:19:55</h3>
                  </div>
                </el-col>
              </el-row>
            </div>
          </el-col>
        </el-row>
      </el-header>
    </div>
    <div id="main">

    </div>-->
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

    <!-- <div style="height:100%">
      <div style="width:60%;float:left">
        <YieldInfo />
      </div>
      <div style="width:40%;float:left">
        <RealTimeInfo />
      </div>
      <div style="width:20%;float:left">
        <BadItemInfo />
      </div>
      <div style="width:20%;float:left">
        <DowntimeInfo />
      </div>
      <div style="width:40%;float:left">
        <ImplProcess />
      </div>
    </div>-->
  </div>
</template>

<script>
// import YieldInfo from "./components/YieldInfo";
// import BadItemInfo from "./components/BadItemInfo"; //不良项
// import DowntimeInfo from "./components/DowntimeInfo"; //停机时长
// import ImplProcess from "./components/ImplProcess"; //table
// import RealTimeInfo from "./components/RealTimeInfo"; //实时状态

import PartTop from "./components/PartTop";
import PartMain from "./components/PartMain";
import PartFooter from "./components/PartFooter";

export default {
  name: "App",
  components: {
    PartTop,
    PartMain,
    PartFooter,

    // YieldInfo,
    // BadItemInfo,
    // DowntimeInfo,
    // ImplProcess,
    // RealTimeInfo
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
.el-header,
.el-footer {
  /* background-color: #b3c0d1; */ 
  /* color: #333; */
  /* text-align: center; */
  /* /* line-height: 60px; */
}

.el-main {
  /* background-color: #e9eef3; */
  /* color: #333; */
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
/* 
#title {
  height: 100px;
}
#title h1 {
  color: #4fd9f7;
}
#title h3 {
  float: right;
  color: #4fd9f7;
} */
</style>
