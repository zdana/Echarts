
<template>
  <div>
    <el-card class="box-card">
      <el-table
        :data="tableData"
        style="width: 100%;"
        height="365"
        :header-cell-style="{color:'#4fd9f7'}"
        :row-style="{color:'#4fd9f7'}"
      >
        <el-table-column prop="num" label="序号" min-width="40" max-width="100"></el-table-column>
        <el-table-column prop="proNum" label="工单号" min-width="70" max-width="180"></el-table-column>
        <el-table-column prop="complStatus" label="完成状态" min-width="50" max-width="100"></el-table-column>
        <el-table-column prop="date" label="开始时间"  min-width="60" max-width="100"></el-table-column>
        <el-table-column prop="dateTo" label="完成时间"  min-width="60" max-width="100"></el-table-column>
      </el-table>
    </el-card>
  </div>
</template>

<script>
export default {
  name: "ImplProcess",
  data() {
    return {
      tableData: [
        {
          num: "82",
          proNum: "1008....",
          complStatus: "true",
          date: "2020-03-04",
          dateTo: "2020-03-08"
        },
        {
          num: "83",
          proNum: "1008....",
          complStatus: "true",
          date: "2020-03-04",
          dateTo: "2020-03-08"
        },
        {
          num: "84",
          proNum: "1008....",
          complStatus: "true",
          date: "2020-03-04",
          dateTo: "2020-03-08"
        },
        {
          num: "85",
          proNum: "1008....",
          complStatus: "true",
          date: "2020-03-04",
          dateTo: "2020-03-08"
        },
        {
          num: "86",
          proNum: "1008....",
          complStatus: "true",
          date: "2020-03-04",
          dateTo: "2020-03-08"
        },
        {
          num: "87",
          proNum: "1008....",
          complStatus: "true",
          date: "2020-03-04",
          dateTo: "2020-03-08"
        },
        {
          num: "88",
          proNum: "1008....",
          complStatus: "true",
          date: "2020-03-04",
          dateTo: "2020-03-08"
        },
        {
          num: "89",
          proNum: "1008....",
          complStatus: "true",
          date: "2020-03-04",
          dateTo: "2020-03-08"
        }
      ]
    };
  }
};
</script>
<style>
.el-table,
.el-table__expanded-cell {
  background-color: transparent;
}

.el-table th,
.el-table tr {
  background-color: transparent;
}
/* .el-table-column{
  background-color: rgba(14, 33, 44, 0.5);
} */

.el-table--border:after,
.el-table--group:after,
.el-table:before {
  background-color: rgba(4, 33, 56, 0.5);
}

.el-table--border,
.el-table--group {
  border-color: rgba(4, 33, 56, 0.5);
}

.el-table td,
.el-table th.is-leaf {
  border-bottom: 1px solid rgba(4, 33, 56, 0.5);
}
</style>
