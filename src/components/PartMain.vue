<template>
  <div id="partMain">
    <el-row>
      <el-col :span="6">
        <el-card class="box-card" style="line-height:30px">
          <el-row>
            <el-col :span="24">
              <el-row>
                <el-col :span="12">
                  <div>
                    <h3>工单号</h3>
                    <h1>270902-1</h1>
                  </div>
                </el-col>
                <el-col :span="12">
                  <div>
                    <h3>达成率</h3>
                    <h1>79%</h1>
                  </div>
                </el-col>
              </el-row>
              <el-row>
                <el-col :span="24">
                  <h3>产品信息</h3>
                  <h1>112501 RZFF618DBALZ</h1>
                </el-col>
              </el-row>
            </el-col>
          </el-row>
        </el-card>
      </el-col>
      <el-col :span="6">
        <el-card class="box-card" style="line-height:30px">
          <el-row>
            <el-col :span="24">
              <el-row>
                <el-col :span="12">
                  <div>
                    <h3>工单数</h3>
                    <h1>2000</h1>
                  </div>
                </el-col>
                <el-col :span="12">
                  <div>
                    <h3>完成数</h3>
                    <h1>1068</h1>
                  </div>
                </el-col>
              </el-row>
              <el-row>
                <el-col :span="12">
                  <h3>开工时间</h3>
                  <h3>
                    2020/03/04
                    <br />08:00:00
                  </h3>
                </el-col>
                <el-col :span="12">
                  <h3>完工时间</h3>
                  <h3>
                    2020/03/04
                    <br />17:00:00
                  </h3>
                </el-col>
              </el-row>
            </el-col>
          </el-row>
        </el-card>
      </el-col>
      <el-col :span="6">
        <BadItemInfo />
      </el-col>
      <el-col :span="6">
        <DowntimeInfo />
      </el-col>
    </el-row>
  </div>
</template>

<script>
import DowntimeInfo from "./DowntimeInfo";
import BadItemInfo from "./BadItemInfo";

export default {
  name: "PartMain",
  components: { DowntimeInfo, BadItemInfo },
  data() {
    return {};
  },
};
</script>
<style>
#partMain .el-col {
  border-radius: 4px;
  padding-left: 10px;
  padding-right: 10px;
  padding-bottom: 10px;
  float: left;
}
#partMain .el-col .el-card {
  width: 100%;
  min-height: 200px;
  max-height: 320px;
  line-height: 60px;
}
#partMain .el-col .el-card img {
  max-width: 300px;
}
</style>