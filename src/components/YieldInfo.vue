<!--
含以下：
    STM 3号线/日产量/实际人数/工单号/工单数/线长/良品率/时间稼动率
-->
<template>
  <div id="part">
    <el-container>
      <el-container>
        <el-aside>
          <el-card style="height:30%;padding:0">
            <img src="../assets/background.jpg" style="padding:0;margin:0" />
            <div style="height:10%;line-height:30px">
              <h3>线长：李江丽</h3>
            </div>
          </el-card>
          <el-card class="box-card" style="height:20%;line-height:30px">
            <h3>SMT3号线</h3>
            <h3>运行</h3>
          </el-card>
          <el-card class="box-card" style="height:20%;line-height:30px">
            <h3>日产量/日定额</h3>
            <h3>738/3498 pcs</h3>
          </el-card>
          <el-card class="box-card" style="height:20%;line-height:30px">
            <h3>实际/标准人数</h3>
            <h3>3/3</h3>
          </el-card>
        </el-aside>
        <el-container>
          <el-main>
            <el-row>
              <el-col :span="12">
                <div class="grid-content bg-purple">
                  <el-card
                    class="box-card"
                    style="margin-right:10px;margin-top:-20px;line-height:60px;"
                  >
                    <h5>工单号</h5>
                    <h3>270902-1</h3>
                    <el-divider></el-divider>
                    <h5>达成率</h5>
                    <h3>79%</h3>
                    <el-divider></el-divider>
                    <h5>产品信息</h5>
                    <h3>112501</h3>
                    <h3>RZFF618DBALZ</h3>
                  </el-card>
                </div>
              </el-col>
              <el-col :span="12">
                <div class="grid-content bg-purple-light">
                  <el-card
                    class="box-card"
                    style="margin-left:10px;margin-top:-20px;line-height:46px"
                  >
                    <h5>工单数</h5>
                    <h3>2000</h3>
                    <el-divider ></el-divider>
                    <h5>完成数</h5>
                    <h3>1068</h3>
                    <el-divider></el-divider>
                    <h5>开工时间</h5>
                    <h3>2020/03/08:00:00</h3>
                    <el-divider></el-divider>
                    <h5>完工时间</h5>
                    <h3>2020/03/17:00:00</h3>
                  </el-card>
                </div>
              </el-col>

              <el-col :span="12">
                <div class="grid-content bg-purple">
                  <el-card class="box-card" style="margin-right:10px;;line-height:30px">
                    <h3>良品率</h3>
                    <h3>99.3%</h3>
                  </el-card>
                </div>
              </el-col>
              <el-col :span="12">
                <div class="grid-content bg-purple-light">
                  <el-card class="box-card" style="margin-left:10px;;line-height:30px">
                    <h3>时间稼动率</h3>
                    <h3>99.1%</h3>
                  </el-card>
                </div>
              </el-col>
            </el-row>
          </el-main>
        </el-container>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "yieldInfo",
  data() {
    return {
      radio: "1"
    };
  },
  mounted() {
    this.axios
      .get("http://122.224.37.226:8093/ASWEB.asmx/eChart_SalesAnalysis", {
        params: {
          date: "2018-1-1",
          dateto: "2020-3-2"
        }
      })
      .then(Response => {
        this.data = Response;
        console.log(this.data);
      });
  }
};
</script>
<style>
.el-footer {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  height:auto
}
.el-aside {
  /* background-color: #d3dce6; */
  color: #333;
  text-align: center;
  height: 100%;
  overflow: hidden;
}

.el-main {
  /* background-color: #e9eef3; */
  color: #333;
  text-align: center;
  margin:0px;
  padding:0
  /* line-height: 160px; */
}

body > .el-container {
  /* margin-bottom: 40px; */
}

.el-card {
  /* margin-bottom: 20px; */
  /* background-color:#333; */
  background-color: rgba(4, 33, 56, 0.5);
  border: none
  
}
.el-card h3,.el-card h5{
  color: rgb(79, 217, 247);
}

.el-card img {
  width: 100%;
  /* height: 180px; */
  /* height: 200px; */
}

.el-divider{
  background-color: #a8a8a8;
}
</style>
