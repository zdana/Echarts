<template>
  <div id="partFooter">
    <el-row>
      <el-col :span="6">
        <el-card class="box-card" style="line-height:20px">
          <h1>良品率</h1>
          <h1>99.3%</h1>
          <el-divider></el-divider>
          <h1>时间稼动率</h1>
          <h1>99.1%</h1>
        </el-card>
      </el-col>
      <el-col :span="12">
        <el-card class="box-card">
          <h1>实时状态</h1>
        </el-card>
      </el-col>
      <el-col :span="6">
        <ImplProcess/>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import ImplProcess from "./ImplProcess";
export default {
  name: "PartFooter",
  components: { ImplProcess },
  data() {
    return {
      radio: "1"
    };
  },
  mounted() {}
};
</script>
<style>
#partFooter .el-col {
  border-radius: 4px;
  padding-left: 10px;
  padding-right: 10px;
  float: left;
}
#partFooter .el-col .el-card {
  width: 100%;
  min-height: 250px;
  max-height: 250px;
  line-height: 60px;
}
</style>

