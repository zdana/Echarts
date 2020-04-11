<template>
  <div id="partTop">
    <el-row>
      <el-col :span="6">
        <div class="grid-content bg-purple">
          <el-card class="box-card" style>
            <h1>SMT3号线</h1>
            <h1>运行</h1>
          </el-card>
        </div>
      </el-col>
      <el-col :span="6">
        <div>
          <el-card class="box-card">
            <h1>日产量/日定额</h1>
            <h1>738/3498 pcs</h1>
          </el-card>
        </div>
      </el-col>
      <el-col :span="6">
        <div>
          <el-card class="box-card">
            <h1>实际/标准人数</h1>
            <h1>3/3</h1>
          </el-card>
        </div>
      </el-col>
      <el-col :span="6">
        <div>
          <el-card style="padding:0;margib:0">
            <img src="../assets/background.jpg" style="padding:0;margin:0;float:right" />
            <div>
              <h1>线长</h1>
              <h1>李江丽</h1>
            </div>
          </el-card>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "partTop",
  data() {
    return {
      radio: "1"
    };
  },
  mounted() {}
};
</script>
<style>
#partTop .el-col {
  border-radius: 4px;
  padding-left: 10px;
  padding-right: 10px;
  padding-bottom:10px ;
  float: left;
}
#partTop .el-col .el-card {
  width: 100%;
  min-height: 100px;
  max-height: 250px;
  line-height: 300%;
}
#partTop .el-col .el-card img {
  max-width: 200px;
}

</style>
