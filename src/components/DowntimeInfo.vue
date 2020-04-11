<!--
含以下：
    停机时长
-->
<template>
  <div>
    <el-card class="box-card">
      <h3  style="color:#a8a8a8">停机时长</h3>
       <div id="myChart2" :style="{width: '300px', height: '190px'}"></div>
    </el-card>
  </div>
</template>

<script>
export default {
  name: "DowntimeInfo",
  data() {
    return {};
  },
   mounted() {
    this.drawLine();
  },
  methods: {
    drawLine() {
      // 基于准备好的dom，初始化echarts实例
      let myChart = this.$echarts.init(document.getElementById("myChart2"));

      var myColor = ["#00c0e9", "#0096f3", "#33CCFF", "#33FFCC"];
      // 绘制图表
      myChart.setOption({
        // title: { text: "停机时长TOP 5 (min)", color:"white" },
       grid: {
          left: '11%',
          top: '',
          right: "0%",
          bottom: "10%",
        containLabel: true
    },
    xAxis: [{
        show: false,
    }],
    yAxis: [{
        axisTick: 'none',
        axisLine: 'none',
        offset: '27',
        axisLabel: {
            textStyle: {
                color: 'color: rgb(79, 217, 247);',
                fontSize: '16',
            }
        },
        data: ['', '', '', '设备维护','等待配送']
    }, {
        axisTick: 'none',
        axisLine: 'none',
        axisLabel: {
            textStyle: {
                color: '',
                fontSize: '16',
            }
        },
        data: ['5', '4', '3', '2', '1']
    }, {
        nameGap: '50',
        nameTextStyle: {
            color: '#ffffff',
            fontSize: '16',
        },
        axisLine: {
            lineStyle: {
                color: 'rgba(0,0,0,0)'
            }
        },
        data: [],
    }],
    series: [{
            name: '条',
            type: 'bar',
            yAxisIndex: 0,
            data: [, , ,7,25 ],
            label: {
                normal: {
                    show: true,
                    position: 'right',
                    textStyle: {
                        color: '#4fd9f7',
                        fontSize: '16',
                    }
                }
            },
            barWidth: 12,
            itemStyle: {
                normal: {
                    color: function(params) {
                        var num = myColor.length;
                        return myColor[params.dataIndex % num]
                    },
                }
            },
            z: 2
        }, {
            name: '白框',
            type: 'bar',
            yAxisIndex: 1,
            barGap: '-100%',
            data: [99, 99.5, 99.5, 99.5,99.5],
            barWidth: 20,
            itemStyle: {
                normal: {
                    color: 'rgba(4, 33, 56, 1)',
                    barBorderRadius: 5,
                }
            },
            z: 1
        }, {
            name: '外框',
            type: 'bar',
            yAxisIndex: 2,
            barGap: '-100%',
            data: [100, 100, 100, 100,100],
            barWidth: 24,
            itemStyle: {
                normal: {
                    color: function(params) {
                        var num = myColor.length;
                        return myColor[params.dataIndex % num]
                    },
                    barBorderRadius: 5,
                }
            },
            z: 0
        },
        {
            name: '外圆',
            type: 'scatter',
            hoverAnimation: false,
            data: [0, 0, 0, 0,0],
            yAxisIndex: 2,
            symbolSize: 15,
            itemStyle: {
                normal: {
                    color: function(params) {
                        var num = myColor.length;
                        return myColor[params.dataIndex % num]
                    },
                    opacity: 1,
                }
            },
            z: 2
        }
    ]
      });
    }
  }
};
</script>
<style>
.el-card {
  margin-bottom: 20px;
  margin-left: 10px;
}
</style>
