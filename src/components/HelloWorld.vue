<template>
  <div class="hello">
   <div id="myChart" :style="{width: '300px', height: '300px'}"></div>
     <el-row>
      <el-col :span="8">111</el-col>
      <el-col :span="8">222</el-col>
      <el-col :span="8">333</el-col>
    </el-row>

  </div>
</template>

<script>
 // 引入基本模板
  let echarts = require("echarts/lib/echarts");
  // 引入柱状图组件
  require("echarts/lib/chart/bar");
  // 引入提示框和title组件
  require("echarts/lib/component/tooltip");
  require("echarts/lib/component/title");
export default {
  name: 'hello',
  data () {
    return {
      msg: '欢迎来到我的简历'
    }
  },
  mounted() {
      this.drawLine();
  },
  methods: {
      drawLine(){
          //初始化ECharts实例
          let myChart = this.$echarts.init(document.getElementById('myChart'))
          //绘制图表
          myChart.setOption({
              title: { text: '在Vue中使用echarts' },
            tooltip: {},
            xAxis: {
                data: ["衬衫","羊毛衫","雪纺衫","裤子","高跟鞋","袜子"]
            },
            yAxis: {},
            series: [{
                name: '销量',
                type: 'bar',
                data: [5, 20, 36, 10, 10, 20]
            }]
          })
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
