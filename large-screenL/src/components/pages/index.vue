<template>
  <div class="wrap">
    <div class="top">
      <div class="imgDiv">
        <img src="../../../static/img/logo@2x.png" alt />
      </div>
      <div class="secondDive">
        <div class="line">
          <img src="../../../static/img/topLine.png" alt />
        </div>
        <div class="topTitle">城市绿地智能监测与质量评估监测系统</div>
      </div>
      <div class="timeThree">
        <div class="time1">{{nowTime}}</div>
        <div class="dayTime">{{nowDate}}</div>
      </div>
      <div class="fourDiv">
        <ul>
          <li>
            <div class="cutDiv">
              <img src="../../../static/img/shujuhuizong@2x.png" alt />
            </div>
            <span class="cutspan">数据汇总</span>
          </li>
          <li>
            <div class="cutDiv">
              <img src="../../../static/img/jichushuju-copy-copy@2x.png" alt />
            </div>
            <span class="cutspan">基础数据</span>
          </li>
          <li>
            <div class="cutDiv">
              <img src="../../../static/img/dongtai@2x.png" alt />
            </div>
            <span class="cutspan">光谱动态</span>
          </li>
          <li>
            <div class="cutDiv">
              <img src="../../../static/img/navshujuduibi@2x.png" alt />
            </div>
            <span class="cutspan">数据对比</span>
          </li>
        </ul>
      </div>
    </div>
    <div class="conter">
      <div class="leftCont">
        <div class="highlight">
          <div class="titileName">高光谱图像</div>
          <div class="reveal">
            <div class="gaoguang">
              <div class="leftgao">
                <img src="../../../static/img/gaoguang.png" alt />
                <span>高光谱图像</span>
              </div>

              <div class="pgNumber">
                <div>
                  <span class="sp1"><countTo ref='example' :startVal='startVal' :endVal='endVal' :duration='4000' :separator='separator'></countTo></span>
                  <span class="sp2">张</span>
                </div>
              </div>
            </div>
            <div class="joint">
              <div class="leftgao">
                <img src="../../../static/img/pinjie.png" alt />
                <span>拼接区域图像</span>
              </div>

              <div class="pgNumber">
                <div>
                  <span class="sp1"><countTo ref='example2' :startVal='startVal' :endVal='endValt' :duration='4000' :separator='separator'></countTo></span>
                  <span class="sp2">张</span>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="qualityTest">
          <div class="titileName">绿地质量检测</div>
          <div class="reveal">
            <!-- <div class="index">
              <div class="indexLeft">
                <span class="spTitle">今日绿地质量指数</span>
                <div class="minfontvat">
                  <span class="sum">6.9</span>
                  <div class="level">
                    <span class="sp1">土地等级</span>
                    <span class="sp2">二级</span>
                  </div>
                </div>
              </div>
              <div class="indexRight">优</div>
            </div>
            <div class="phsum">
              <span class="titlePh">绿地PH值</span>
              <ul>
                <li class="li1">
                  <div></div>
                  <span>3</span>
                </li>
                <li class="li2">
                  <div></div>
                  <span>4</span>
                </li>
                <li class="li3">
                  <div></div>
                  <span>5</span>
                </li>
                <li class="li4">
                  <div></div>
                  <span>6</span>
                </li>
                <li class="li5">
                  <div></div>
                  <span>7</span>
                </li>
                <li class="li6">
                  <div></div>
                  <span>8</span>
                </li>
                <li class="li7">
                  <div></div>
                  <span>9</span>
                </li>
                <li class="li8">
                  <div></div>
                  <span>10</span>
                </li>
              </ul>
              <div class="verticalIcon">
                 <img src="../../../static/img/PHicon.png" alt=""> 
              </div>
            </div>-->
            <div class="state">
              <div class="soil">
                <img class="leftimg" src="../../../static/img/walter.png" alt />
                <div class="right">
                  <span class="trspan">土壤水分</span>
                  <div class="numbertr">
                    <span class="number">39%</span>
                    <div class="gradient">
                      <img src="../../../static/img/arrow-x.png" alt />
                      <span>1%</span>
                    </div>
                  </div>
                </div>
              </div>
              <div class="temperature">
                <img class="leftimg" src="../../../static/img/wdj.png" alt />
                <div class="right">
                  <span class="trspan">土壤温度</span>
                  <div class="numbertr">
                    <span class="number">19°C</span>
                    <div class="gradientgreen">
                      <img src="../../../static/img/arrow-s.png" alt />
                      <span>1%</span>
                    </div>
                  </div>
                </div>
              </div>
              <div class="organic">
                <img class="leftimg2" src="../../../static/img/yjw.png" alt />
                <div class="right">
                  <span class="trspan">有机物质</span>
                  <div class="numbertr">
                    <span class="number">39°C</span>
                    <div class="gradientgreen">
                      <!-- <img src="../../../static/img/arrow-s.png" alt /> -->
                      <div></div>
                      <!-- <span>1%</span> -->
                    </div>
                  </div>
                </div>
              </div>
              <div class="muriate">
                <img class="leftimg2" src="../../../static/img/lhw.png" alt />
                <div class="right">
                  <span class="trspan">氯化物</span>
                  <div class="numbertr">
                    <span class="number">3.9g</span>
                    <div class="gradientgreen">
                      <!-- <img src="../../../static/img/arrow-s.png" alt /> -->
                      <div></div>
                      <!-- <span>1%</span> -->
                    </div>
                  </div>
                </div>
              </div>
              <div class="mineral">
                <img class="leftimg2" src="../../../static/img/kwy.png" alt />
                <div class="right">
                  <span class="trspan">矿物油</span>
                  <div class="numbertr">
                    <span class="number">13.9g</span>
                    <div class="gradientgreen">
                      <!-- <img src="../../../static/img/arrow-s.png" alt /> -->
                      <div></div>
                      <!-- <span>1%</span> -->
                    </div>
                  </div>
                </div>
              </div>
              <div class="fluoride">
                <img class="leftimg2" src="../../../static/img/kwy.png" alt />
                <div class="right">
                  <span class="trspan">氟化物</span>
                  <div class="numbertr">
                    <span class="number">1.9g</span>
                    <div class="gradientgreen">
                      <!-- <img src="../../../static/img/arrow-s.png" alt /> -->
                      <div></div>
                      <!-- <span>1%</span> -->
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="detection">
          <div class="titileName">检测统计数据</div>
          <div class="reveal">
            <div class="state">
              <div class="soil">
                <img class="leftimg" src="../../../static/img/walter.png" alt />
                <div class="right">
                  <span class="trspan">负氧离子</span>
                  <div class="numbertr">
                    <span class="number">219</span>
                    <div class="gradient">
                      <img src="../../../static/img/arrow-x.png" alt />
                      <span>1%</span>
                    </div>
                  </div>
                </div>
              </div>
              <div class="temperature">
                <img class="leftimg" src="../../../static/img/wdj.png" alt />
                <div class="right">
                  <span class="trspan">CO指标</span>
                  <div class="numbertr">
                    <span class="number">19°C</span>
                    <div class="gradientgreen">
                      <img src="../../../static/img/arrow-s.png" alt />
                      <span>1%</span>
                    </div>
                  </div>
                </div>
              </div>
              <div class="organic">
                <img class="leftimg2" src="../../../static/img/yjw.png" alt />
                <div class="right">
                  <span class="trspan">O3指标</span>
                  <div class="numbertr">
                    <span class="number">39°C</span>
                    <div class="gradientgreen">
                      <!-- <img src="../../../static/img/arrow-s.png" alt /> -->
                      <div></div>
                      <!-- <span>1%</span> -->
                    </div>
                  </div>
                </div>
              </div>
              <div class="muriate">
                <img class="leftimg2" src="../../../static/img/lhw.png" alt />
                <div class="right">
                  <span class="trspan">PM2.5</span>
                  <div class="numbertr">
                    <span class="number">3.9g</span>
                    <div class="gradientgreen">
                      <!-- <img src="../../../static/img/arrow-s.png" alt /> -->
                      <div></div>
                      <!-- <span>1%</span> -->
                    </div>
                  </div>
                </div>
              </div>
              <div class="mineral">
                <img class="leftimg2" src="../../../static/img/kwy.png" alt />
                <div class="right">
                  <span class="trspan">PM10</span>
                  <div class="numbertr">
                    <span class="number">77.4</span>
                    <div class="gradientgreen">
                      <!-- <img src="../../../static/img/arrow-s.png" alt /> -->
                      <div></div>
                      <!-- <span>1%</span> -->
                    </div>
                  </div>
                </div>
              </div>
              <div class="fluoride">
                <img class="leftimg2" src="../../../static/img/kwy.png" alt />
                <div class="right">
                  <span class="trspan">TVOCs</span>
                  <div class="numbertr">
                    <span class="number">0.3</span>
                    <div class="gradientgreen">
                      <!-- <img src="../../../static/img/arrow-s.png" alt /> -->
                      <div></div>
                      <!-- <span>1%</span> -->
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="middleCont">
        <div class="mapconter">
          <img src="../../../static/img/map.png" alt />
        </div>
        <div class="chart">
          <div class="dateClassify">
            <ul>
              <li>按年</li>
              <li>按季度</li>
              <li>按月</li>
            </ul>
          </div>
          <div class="chartlist">
            <div class="OxygenIons">
              <div class="toptit">负氧离子</div>
              <div class="lintg" ref="OxygenIons"></div>
            </div>
            <div class="OxygenIons">
              <div class="toptit">土壤数据</div>
              <div class="lintg" ref="soilData"></div>
            </div>
            <div class="OxygenIons">
              <div class="toptit">碳汇数据</div>
              <div class="lintg" ref="carbonData"></div>
            </div>
            <div class="OxygenIons">
              <div class="toptit">植物密度</div>
              <div class="lintg" ref="botanyData"></div>
            </div>
          </div>
        </div>
      </div>
      <div class="rightCont">
        <div class="OxygenIons">
          <div class="toptit">健康指标</div>
          <span class="titlehealth">近一年绿地健康指标趋势</span>
          <div class="lintg" ref="healthData"></div>
        </div>
        <div class="OxygenIons">
          <div class="toptit">体征数据</div>
          <div class="lintg" ref="signData"></div>
        </div>
        <div class="grade">
          <img src="../../../static/img/pgfen.png" alt />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import countTo from 'vue-count-to';
export default {
  components: {countTo},
  data() {
    return {
      chart: null,
      nowDate: "", // 当前日期
      nowTime: "", // 当前时间
      nowWeek: "", // 当前星期
         // 初始值
        startVal: 0,
        // 最终值
        endVal: 1089,
        endValt: 1089,
        separator:''
    };
  },

  beforeCreate() {
    //页面加载前
  },
  created() {
    //页面加载完成
  },
  beforeMount() {
    //组件载入前
  },
  mounted() {
    //组件载入后
    this.$refs.example.start();
    this.$refs.example2.start();
    this.$nextTick(function () {
      this.chartinit();
      this.chartinitsoil();
      this.chartinitcarbon();
      this.chartinitbotany();
      this.chartinithealth();
      this.chartinitsign();
    });
    this.currentTime();
    //自适应
    // let _this = this;
    // window.onresize = function () {
    //   _this.chartinit.resize();
    //   _this.chartinitsoil.resize();
    //   _this.chartinitcarbon.resize();
    //   _this.chartinitbotany.resize();
    //   _this.chartinithealth.resize();
    //   _this.chartinitsign.resize();
    // };
  },
  methods: {
    //时间刷新
    currentTime() {
      setInterval(this.getDate, 500);
    },
    //时间获取

    getDate: function () {
      var _this = this;
      let yy = new Date().getFullYear();
      let mm = new Date().getMonth() + 1;
      let dd = new Date().getDate();
      let week = new Date().getDay();
      let hh = new Date().getHours();
      let mf =
        new Date().getMinutes() < 10
          ? "0" + new Date().getMinutes()
          : new Date().getMinutes();
      let ms = new Date().getSeconds();
      if (week == 1) {
        this.nowWeek = "星期一";
      } else if (week == 2) {
        this.nowWeek = "星期二";
      } else if (week == 3) {
        this.nowWeek = "星期三";
      } else if (week == 4) {
        this.nowWeek = "星期四";
      } else if (week == 5) {
        this.nowWeek = "星期五";
      } else if (week == 6) {
        this.nowWeek = "星期六";
      } else {
        this.nowWeek = "星期日";
      }
      _this.nowTime = hh + ":" + mf + ":"+ ms;
      _this.nowDate = yy + "." + mm + "." + dd;
    },
    chartinit(data) {
      this.chart = this.$echarts.init(this.$refs.OxygenIons);
      var array = [80, 92, 101, 144];
      this.chart.setOption({
        xAxis: {
          type: "category",
          boundaryGap: false,
          axisLabel: {
            textStyle: {
              fontSize: 12,
              color: "#A2D4E5",
            },
          },

          data: ["一季度", "二季度", "三季度", "四季度"],
        },
        yAxis: {
          type: "value",
          axisLabel: {
            textStyle: {
              fontSize: 10,
              color: "#A2D4E5",
            },
          },
          splitLine: {
            lineStyle: {
              // 使用深浅的间隔色
              color: ["#0E1B29"],
            },
          },
        },
        tooltip: {
          trigger: "axis",
          axisPointer: {
            type: "cross",
            crossStyle: {
              color: "#0E1B29",
            },
          },
          formatter: function (array) {
            // console.log(params); // 当我们想要自定义提示框内容时，可以先将鼠标悬浮的数据打印出来，然后根据需求提取出来即可
            // let firstParams = params[0];
            // let sndParams = params[1];
            return array[1];
          },
        },
        grid: {
          top: "13%",
          left: "1%",
          right: "10%",
          bottom: "8%",
          containLabel: true,
        },

        series: [
          {
            data: [80, 92, 101, 144],
            type: "line",
            areaStyle: {
              normal: {
                color: "#034A4A", //改变区域颜色
              },
            },
            itemStyle: {
              normal: {
                color: "#05C6B3", //改变折线点的颜色
                lineStyle: {
                  color: "#05C6B3 ", //改变折线颜色
                },
              },
            },
          },
        ],
      });
    },
    chartinitsoil() {
      this.chart = this.$echarts.init(this.$refs.soilData);
      var array = [80, 92, 101, 144];
      this.chart.setOption({
        xAxis: {
          type: "category",
          boundaryGap: false,
          axisLabel: {
            textStyle: {
              fontSize: 12,
              color: "#A2D4E5",
            },
          },

          data: ["一季度", "二季度", "三季度", "四季度"],
        },
        yAxis: {
          type: "value",
          axisLabel: {
            textStyle: {
              fontSize: 10,
              color: "#A2D4E5",
            },
            splitLine: {
              lineStyle: {
                // 使用深浅的间隔色
                color: ["#0E1B29"],
              },
            },
          },
        },
        tooltip: {
          trigger: "axis",
          axisPointer: {
            type: "cross",
            crossStyle: {
              color: "#fff",
            },
          },
          formatter: function (array) {
            // console.log(params); // 当我们想要自定义提示框内容时，可以先将鼠标悬浮的数据打印出来，然后根据需求提取出来即可
            // let firstParams = params[0];
            // let sndParams = params[1];
            return array[1];
          },
        },
        grid: {
          top: "13%",
          left: "0%",
          right: "10%",
          bottom: "8%",
          containLabel: true,
        },

        series: [
          {
            data: [30, 12, 38, 87],
            type: "line",
            areaStyle: {
              normal: {
                color: "#034A4A", //改变区域颜色
              },
            },
            itemStyle: {
              normal: {
                color: "#073459", //改变折线点的颜色
                lineStyle: {
                  color: "#073459", //改变折线颜色
                },
              },
            },
          },
        ],
      });
    },
    chartinitcarbon() {
      this.chart = this.$echarts.init(this.$refs.carbonData);
      var array = [80, 92, 101, 144];
      this.chart.setOption({
        xAxis: {
          type: "category",
          boundaryGap: false,
          axisLabel: {
            textStyle: {
              fontSize: 10,
              color: "#A2D4E5",
            },
          },

          data: ["一季度", "二季度", "三季度", "四季度"],
        },
        yAxis: {
          type: "value",
          axisLabel: {
            textStyle: {
              fontSize: 12,
              color: "#A2D4E5",
            },
          },
          splitLine: {
            lineStyle: {
              // 使用深浅的间隔色
              color: ["#0E1B29"],
            },
          },
        },
        tooltip: {
          trigger: "axis",
          axisPointer: {
            type: "cross",
            crossStyle: {
              color: "#fff",
            },
          },
          formatter: function (array) {
            // console.log(params); // 当我们想要自定义提示框内容时，可以先将鼠标悬浮的数据打印出来，然后根据需求提取出来即可
            // let firstParams = params[0];
            // let sndParams = params[1];
            return array[1];
          },
        },
        grid: {
          top: "13%",
          left: "0%",
          right: "10%",
          bottom: "8%",
          containLabel: true,
        },

        series: [
          {
            data: [30, 42, 38, 67],
            type: "line",
            areaStyle: {
              normal: {
                color: "#5549A1", //改变区域颜色
              },
            },
            itemStyle: {
              normal: {
                color: "#242953", //改变折线点的颜色
                lineStyle: {
                  color: "#242953", //改变折线颜色
                },
              },
            },
          },
        ],
      });
    },
    chartinitbotany() {
      this.chart = this.$echarts.init(this.$refs.botanyData);
      var array = [80, 92, 101, 104];
      this.chart.setOption({
        xAxis: {
          type: "category",
          boundaryGap: false,
          axisLabel: {
            textStyle: {
              fontSize: 12,
              color: "#A2D4E5",
            },
          },

          data: ["一季度", "二季度", "三季度", "四季度"],
        },
        yAxis: {
          type: "value",
          axisLabel: {
            textStyle: {
              fontSize: 10,
              color: "#A2D4E5",
            },
          },
          splitLine: {
            lineStyle: {
              // 使用深浅的间隔色
              color: ["#0E1B29"],
            },
          },
        },
        tooltip: {
          trigger: "axis",
          axisPointer: {
            type: "cross",
            crossStyle: {
              color: "#fff",
            },
          },
          formatter: function (array) {
            // console.log(params); // 当我们想要自定义提示框内容时，可以先将鼠标悬浮的数据打印出来，然后根据需求提取出来即可
            // let firstParams = params[0];
            // let sndParams = params[1];
            return array[1];
          },
        },
        grid: {
          top: "13%",
          left: "0%",
          right: "10%",
          bottom: "8%",
          containLabel: true,
        },

        series: [
          {
            data: [20, 52, 48, 57],
            type: "line",
            areaStyle: {
              normal: {
                color: "#585314", //改变区域颜色
              },
            },
            itemStyle: {
              normal: {
                color: "#BFA104", //改变折线点的颜色
                lineStyle: {
                  color: "#BFA104", //改变折线颜色
                },
              },
            },
          },
        ],
      });
    },
    chartinithealth() {
      this.chart = this.$echarts.init(this.$refs.healthData);
      var array = [80, 92, 101, 144];
      this.chart.setOption({
        // title: {
        //   show: true,
        //   text: "近一年绿地覆盖率指标趋势",
        //   textStyle: {
        //     //主标题文本样式{"fontSize": 18,"fontWeight": "bolder","color": "#333"}
        //     fontFamily: "SimHei Regular",
        //     fontSize: 12,
        //     fontStyle: "normal",
        //     fontWeight: "normal",
        //     color: "#A2D4E5"
        //   }
        // },
        xAxis: {
          type: "category",
          boundaryGap: false,
          axisLabel: {
            textStyle: {
              fontSize: 10,
              color: "#A2D4E5",
            },
          },

          data: ["一季度", "二季度", "三季度", "四季度"],
        },
        yAxis: {
          type: "value",
          axisLabel: {
            textStyle: {
              fontSize: 12,
              color: "#A2D4E5",
            },
          },
          splitLine: {
            lineStyle: {
              // 使用深浅的间隔色
              color: ["#0E1B29"],
            },
          },
        },
        tooltip: {
          trigger: "axis",
          axisPointer: {
            type: "cross",
            crossStyle: {
              color: "#fff",
            },
          },
          formatter: function (array) {
            // console.log(params); // 当我们想要自定义提示框内容时，可以先将鼠标悬浮的数据打印出来，然后根据需求提取出来即可
            // let firstParams = params[0];
            // let sndParams = params[1];
            return array[1];
          },
        },
        grid: {
          top: "5%",
          left: "0%",
          right: "10%",
          bottom: "8%",
          containLabel: true,
        },

        series: [
          {
            data: [20, 52, 48, 67],
            type: "line",
            areaStyle: {
              normal: {
                color: "#585314", //改变区域颜色
              },
            },
            itemStyle: {
              normal: {
                color: "#BFA104", //改变折线点的颜色
                lineStyle: {
                  color: "#BFA104", //改变折线颜色
                },
              },
            },
          },
        ],
      });
    },
    chartinitbotany() {
      this.chart = this.$echarts.init(this.$refs.botanyData);
      var array = [80, 92, 101, 10];
      this.chart.setOption({
        xAxis: {
          type: "category",
          boundaryGap: false,
          axisLabel: {
            textStyle: {
              fontSize: 12,
              color: "#A2D4E5",
            },
          },

          data: ["一季度", "二季度", "三季度", "四季度"],
        },
        yAxis: {
          type: "value",
          axisLabel: {
            textStyle: {
              fontSize: 10,
              color: "#A2D4E5",
            },
          },
          splitLine: {
            lineStyle: {
              // 使用深浅的间隔色
              color: ["#0E1B29"],
            },
          },
        },
        tooltip: {
          trigger: "axis",
          axisPointer: {
            type: "cross",
            crossStyle: {
              color: "#fff",
            },
          },
          formatter: function (array) {
            // console.log(params); // 当我们想要自定义提示框内容时，可以先将鼠标悬浮的数据打印出来，然后根据需求提取出来即可
            // let firstParams = params[0];
            // let sndParams = params[1];
            return array[1];
          },
        },
        grid: {
          top: "13%",
          left: "0%",
          right: "10%",
          bottom: "8%",
          containLabel: true,
        },

        series: [
          {
            data: [20, 52, 48, 57],
            type: "line",
            areaStyle: {
              normal: {
                color: "#585314", //改变区域颜色
              },
            },
            itemStyle: {
              normal: {
                color: "#BFA104", //改变折线点的颜色
                lineStyle: {
                  color: "#BFA104", //改变折线颜色
                },
              },
            },
          },
        ],
      });
    },
    chartinitsign() {
      this.chart = this.$echarts.init(this.$refs.signData);
      this.chart.setOption({
        legend: {
          itemWidth: 10,
          itemHeight: 10,
          itemGap: 10,
          top: "5%",
          textStyle: {
            //图例文字的样式
            color: "#A2D4E5",
            fontSize: 10,
          },
        },
        tooltip: {},

        dataset: {
          source: [
            ["product", "含水量", "NPK含量", "叶绿素"],
            ["一季度", 43.3, 85.8, 93.7],
            ["二季度", 83.1, 73.4, 55.1],
            ["三季度", 86.4, 65.2, 82.5],
            ["四季度", 72.4, 53.9, 39.1],
          ],
        },
        xAxis: {
          type: "category",
          boundaryGap: true,
          axisLabel: {
            textStyle: {
              fontSize: 10,
              color: "#A2D4E5",
            },
          },

          // data: ["一季度", "二季度", "三季度", "四季度"]
        },
        yAxis: {
          type: "value",
          axisLabel: {
            textStyle: {
              fontSize: 10,
              color: "#A2D4E5",
            },
          },
          splitLine: {
            lineStyle: {
              // 使用深浅的间隔色
              color: ["#0E1B29"],
            },
          },
        },
        tooltip: {
          trigger: "axis",
          axisPointer: {
            type: "cross",
            crossStyle: {
              color: "#fff",
            },
          },
          formatter: function (array) {
            // console.log(params); // 当我们想要自定义提示框内容时，可以先将鼠标悬浮的数据打印出来，然后根据需求提取出来即可
            // let firstParams = params[0];
            // let sndParams = params[1];
            return array[1];
          },
        },
        grid: {
          top: "23%",
          left: "0%",
          right: "10%",
          bottom: "8%",
          containLabel: true,
        },

        series: [
          {
            type: "bar",
            barGap: 0,
            barWidth: 5,
            itemStyle: { normal: { color: "#08C8B9" } },
          },
          {
            type: "bar",
            barGap: 0,
            barWidth: 5,
            itemStyle: { normal: { color: "#1692FA" } },
          },
          {
            type: "bar",
            barGap: 0,
            barWidth: 5,
            itemStyle: { normal: { color: "#6F75DC" } },
          },
        ],
      });
    },
  },
  beforeDestroy() {
    //组件销毁前
    if (this.getDate) {
      console.log("销毁定时器");
      clearInterval(this.getDate); // 在Vue实例销毁前，清除时间定时器
    }
  },
  destroyed() {
    //组件销毁后
  },
};
</script>
<style lang="scss">
.wrap {
  display: -webkit-flex; /* Chrome 21+, Safari 6.1+, iOS Safari 7+, Opera 15/16 */
  display: -moz-flex; /* Firefox 18+ */
  display: -ms-flexbox; /* IE 10 */
  display: flex; /* Chrome 29+, Firefox 22+, IE 11+, Opera 12.1/17/18, Android 4.4+ */
  height: 100vh;
  flex-direction: column;
  .top {
    height: 122px;
    width: 100%;
    display: -webkit-flex; /* Chrome 21+, Safari 6.1+, iOS Safari 7+, Opera 15/16 */
    display: -moz-flex; /* Firefox 18+ */
    display: -ms-flexbox; /* IE 10 */
    display: flex;

    .imgDiv {
      width: 101px;
      height: 101px;
      margin-left: 38px;
      padding-top: 21px;
      img {
        width: 100%;
        height: 100%;
      }
    }
    .secondDive {
      width: 1146px;
      height: 100px;
      padding-top: 21px;
      margin-left: 15px;
      .line {
        width: 100%;
        height: 25px;
        img {
          width: 100%;
          height: 100%;
        }
      }
      .topTitle {
        height: 42px;
        width: 100%;
        font-family: "Microsoft YaHei Regular";
        font-size: 34px;
        color: #feffff;
        line-height: 42px;
        text-align: left;
      }
    }
    .timeThree {
      width: 200px;
      height: 25px;
      line-height: 25px;
      padding-top: 21px;
      display: -webkit-flex; /* Chrome 21+, Safari 6.1+, iOS Safari 7+, Opera 15/16 */
      display: -moz-flex; /* Firefox 18+ */
      display: -ms-flexbox; /* IE 10 */
      display: flex;
      font-family: "Microsoft YaHei Regular";
      color: #b8edfb;
      .time1 {
        padding-left: 30px;
        font-size: 22px;
        padding-right: 6px;
      }
      .dayTime {
        font-size: 12px;
        padding-right: 30px;
      }
    }
    .fourDiv {
      width: 392px;
      height: 100px;
      ul {
        display: -webkit-flex; /* Chrome 21+, Safari 6.1+, iOS Safari 7+, Opera 15/16 */
        display: -moz-flex; /* Firefox 18+ */
        display: -ms-flexbox; /* IE 10 */
        display: flex;
        li {
          width: 64px;
          height: 80px;
          margin-left: 34px;
          .cutDiv {
            width: 18px;
            height: 18px;
            padding-top: 27px;
            padding-bottom: 10px;
            margin: 0 auto;
            img {
              width: 100%;
              height: 100%;
            }
          }
          .cutspan {
            text-align: center;
            font-size: 14px;
            font-family: "Adobe Heiti Std R";
            color: #a9ddee;
          }
        }
      }
    }
  }
  .conter {
    flex: auto;
    display: -webkit-flex;
    display: -moz-flex;
    display: -ms-flexbox;
    display: flex;
    width: 100%;
    .leftCont {
      width: 330px;
      height: 100%;
      .highlight {
        height: 230px;
        width: 240px;
        margin-left: 37px;
        margin-top: 26px;
        .titileName {
          // width: 100%;
          height: 28px;
          font-family: "Microsoft YaHei Regular";
          font-size: 16px;
          color: #b8edfb;
          padding-left: 7px;
          background: -moz-linear-gradient(to bottom, #013842, 40%, #036574);
          background: -webkit-gradient(to bottom, #013842, 40%, #036574);
          background: -webkit-linear-gradient(to bottom, #013842, 40%, #036574);
          background: -o-linear-gradient(to bottom, #013842, 40%, #036574);
          background: -ms-linear-gradient(to bottom, #013842, 40%, #036574);
          background: linear-gradient(to bottom, #013842, 80%, #036574);
          border-top: 2px solid #067aae;
        }
        .reveal {
          width: 240px;
          height: 200px;
          background: #020d17;
          .gaoguang,
          .joint {
            width: 100%;
            height: 100px;
            display: -webkit-flex;
            display: -moz-flex;
            display: -ms-flexbox;
            display: flex;
            justify-content: space-between;
            .leftgao {
              display: flex;
              img {
                width: 28px;
                height: 30px;
                margin-left: 17px;
                margin-top: 36px;
              }
              span {
                font-family: "Adobe Heiti Std R";
                color: #a9ddee;
                font-size: 14px;
                margin-left: 12px;
                margin-top: 36px;
              }
            }

            .pgNumber {
              width: 60px;
              height: 63px;
              border: 1px solid #035574;
              margin-top: 18px;
              margin-right: 21px;
              div {
                width: 50px;
                height: 62px;
                background: #022433;
                border: 1px solid #035574;
                margin-left: 4px;
                text-align: center;
                font-family: "Adobe Heiti Std R";
                color: #e8ffff;
                .sp1 {
                  font-size: 20px;
                }
                .sp2 {
                  font-size: 11px;
                }
              }
            }
          }
          .joint {
            width: 100%;
            height: 100px;
            display: -webkit-flex;
            display: -moz-flex;
            display: -ms-flexbox;
            display: flex;
            justify-content: space-between;
            .leftgao {
              display: flex;
              img {
                width: 20px;
                height: 18px;
                margin-left: 21px;
                margin-top: 39px;
              }
              span {
                font-family: "Adobe Heiti Std R";
                color: #a9ddee;
                font-size: 14px;
                margin-left: 12px;
                margin-top: 36px;
              }
            }

            .pgNumber {
              width: 60px;
              height: 63px;
              border: 1px solid #035574;
              margin-top: 18px;
              margin-right: 21px;
              div {
                width: 50px;
                height: 62px;
                background: #022433;
                border: 1px solid #035574;
                margin-left: 4px;
                text-align: center;
                font-family: "Adobe Heiti Std R";
                color: #e8ffff;
                .sp1 {
                  font-size: 20px;
                }
                .sp2 {
                  font-size: 11px;
                }
              }
            }
          }
        }
      }
      .qualityTest,
      .detection {
        height: auto;
        width: 240px;
        margin-left: 37px;
        margin-top: 32px;
        .titileName {
          // width: 100%;
          height: 28px;
          font-family: "Microsoft YaHei Regular";
          font-size: 16px;
          color: #b8edfb;
          padding-left: 7px;
          background: -moz-linear-gradient(to bottom, #013842, 40%, #036574);
          background: -webkit-gradient(to bottom, #013842, 40%, #036574);
          background: -webkit-linear-gradient(to bottom, #013842, 40%, #036574);
          background: -o-linear-gradient(to bottom, #013842, 40%, #036574);
          background: -ms-linear-gradient(to bottom, #013842, 40%, #036574);
          background: linear-gradient(to bottom, #013842, 80%, #036574);
          border-top: 2px solid #067aae;
        }
        .reveal {
          width: 100%;
          height: auto;
          background: #020d17;
          .index {
            height: 60px;
            width: auto;
            display: -webkit-flex;
            display: -moz-flex;
            display: -ms-flexbox;
            display: flex;
            margin: 24px 25px 0 15px;
            .indexLeft {
              .spTitle {
                display: block;
                font-family: "Adobe Heiti Std R";
                color: #a9ddee;
                font-size: 14px;
              }
              .minfontvat {
                display: -webkit-flex;
                display: -moz-flex;
                display: -ms-flexbox;
                display: flex;
                .sum {
                  font-size: 28px;
                  color: #a9ddee;
                  font-family: "Adobe Heiti Std R";
                }
                .level {
                  margin-left: 10px;
                  .sp1 {
                    font-size: 10px;
                    color: #a9ddee;
                    display: block;
                    font-family: "Adobe Heiti Std R";
                  }
                  .sp2 {
                    font-size: 14px;
                    color: #05ff51;
                    display: block;
                    font-family: "Adobe Heiti Std R";
                  }
                }
              }
            }
            .indexRight {
              height: 59px;
              width: 54px;
              border: 2px solid #424a5d;
              font-family: "Adobe Heiti Std R";
              font-size: 28px;
              color: #a9ddee;
              line-height: 59px;
              text-align: center;
              margin-left: 20px;
            }
          }
          .phsum {
            width: auto;
            height: 90px;
            margin: 20px 23px 0 15px;
            position: relative;
            .titlePh {
              color: #a9ddee;
              font-size: 10px;
              font-family: "Adobe Heiti Std R";
            }
            ul {
              display: -webkit-flex;
              display: -moz-flex;
              display: -ms-flexbox;
              display: flex;
            }
            ul li {
              width: 24px;
              height: 20px;
              margin-right: 2px;

              span {
                font-family: "Adobe Heiti Std R";
                font-size: 10px;
                color: #a9ddee;
              }
            }
            .li1 {
              div {
                width: 100%;
                height: 6px;
                background: #3b7cff;
              }
            }
            .li2 {
              div {
                width: 100%;
                height: 6px;
                background: #3bbcff;
              }
            }
            .li3 {
              div {
                width: 100%;
                height: 6px;
                background: #29adb5;
              }
            }
            .li4 {
              div {
                width: 100%;
                height: 6px;
                background: #05ff51;
              }
            }
            .li5 {
              div {
                width: 100%;
                height: 6px;
                background: #a1ff05;
              }
            }
            .li6 {
              div {
                width: 100%;
                height: 6px;
                background: #ffc002;
              }
            }
            .li7 {
              div {
                width: 100%;
                height: 6px;
                background: #e51104;
              }
            }
            .li8 {
              div {
                width: 100%;
                height: 6px;
                background: #ab0c37;
              }
            }
            .verticalIcon {
              width: 4px;
              height: 70px;
              position: absolute;
              left: 87px;
              top: -10px;
              background: #577182;
              border-top-right-radius: 5px;
              border-top-left-radius: 5px;
              border-bottom-left-radius: 5px;
              border-bottom-right-radius: 5px;
              img {
                width: 100%;
                height: 100%;
              }
            }
          }
          .state {
            padding: 20px 25px 10px 18px;
            display: -webkit-flex;
            display: -moz-flex;
            display: -ms-flexbox;
            display: flex;
            flex-wrap: wrap;

            justify-content: space-between;
            .soil,
            .temperature,
            .organic,
            .muriate,
            .mineral,
            .fluoride {
              display: -webkit-flex;
              display: -moz-flex;
              display: -ms-flexbox;
              display: flex;
              margin-bottom: 25px;
              width: 90px;
              .leftimg {
                width: 21px;
                height: 28px;
                margin: 5px 8px 0 0;
              }
              .leftimg2 {
                width: 28px;
                height: 28px;
                margin: 5px 8px 0 0;
              }
              .right {
                .trspan {
                  font-family: "Adobe Heiti Std R";
                  font-size: 10px;
                  color: #a9ddee;
                }
                .numbertr {
                  display: flex;
                  .number {
                    font-family: "Adobe Heiti Std R";
                    font-size: 14px;
                    color: #a9ddee;
                    margin-right: 5px;
                  }
                  .gradient {
                    display: -webkit-flex;
                    display: -moz-flex;
                    display: -ms-flexbox;
                    display: flex;
                    img {
                      height: 15px;
                      width: 13px;
                      margin-top: 3px;
                    }
                    span {
                      font-family: "SimHei Regular";
                      color: #fb8a37;
                      font-size: 12px;
                      line-height: 15px;
                      margin-top: 3px;
                    }
                  }
                  .gradientgreen {
                    display: -webkit-flex;
                    display: -moz-flex;
                    display: -ms-flexbox;
                    display: flex;
                    div {
                      width: 5px;
                      height: 1px;
                      background: #04cd43;
                      margin-top: 10px;
                    }
                    img {
                      height: 15px;
                      width: 13px;
                      margin-top: 3px;
                    }
                    span {
                      font-family: "SimHei Regular";
                      color: #04cd43;
                      font-size: 12px;
                      line-height: 15px;
                      margin-top: 3px;
                    }
                  }
                }
              }
            }
          }
        }
      }
    }
    .middleCont {
      width: 1222px;
      height: 100%;
      .mapconter {
        width: 100%;
        height: 63%;
        img {
          width: 100%;
          height: 100%;
        }
      }
      .chart {
        width: 100%;
        height: auto;
        .dateClassify {
          width: 100%;
          height: 40px;
          margin-bottom: 20px;
          ul {
            display: -webkit-flex;
            display: -moz-flex;
            display: -ms-flexbox;
            display: flex;
            li {
              height: 40px;
              width: 95px;
              line-height: 40px;
              text-align: center;
              color: #b8edfb;
              margin-right: 10px;
              border: 2px solid #08b9f4;
            }
          }
        }
        .chartlist {
          display: -webkit-flex;
          display: -moz-flex;
          display: -ms-flexbox;
          display: flex;
          .OxygenIons {
            width: 300px;
            height: 230px;
            margin-right: 8px;

            .toptit {
              height: 28px;
              font-family: "Microsoft YaHei Regular";
              font-size: 16px;
              color: #b8edfb;
              padding-left: 7px;
              background: -moz-linear-gradient(
                to bottom,
                #013842,
                40%,
                #036574
              );
              background: -webkit-gradient(to bottom, #013842, 40%, #036574);
              background: -webkit-linear-gradient(
                to bottom,
                #013842,
                40%,
                #036574
              );
              background: -o-linear-gradient(to bottom, #013842, 40%, #036574);
              background: -ms-linear-gradient(to bottom, #013842, 40%, #036574);
              background: linear-gradient(to bottom, #013842, 80%, #036574);
              border-top: 2px solid #067aae;
            }

            .lintg {
              width: 100%;
              height: 195px;
            }
          }
        }
      }
    }
    .rightCont {
      width: 350px;
      height: 100%;
      position: relative;
      .OxygenIons {
        width: 280px;
        height: 270px;
        margin-left: 20px;

        margin-top: 26px;
        background: #020d17;
        .toptit {
          height: 28px;
          font-family: "Microsoft YaHei Regular";
          font-size: 16px;
          color: #b8edfb;
          padding-left: 7px;
          background: -moz-linear-gradient(to bottom, #013842, 40%, #036574);
          background: -webkit-gradient(to bottom, #013842, 40%, #036574);
          background: -webkit-linear-gradient(to bottom, #013842, 40%, #036574);
          background: -o-linear-gradient(to bottom, #013842, 40%, #036574);
          background: -ms-linear-gradient(to bottom, #013842, 40%, #036574);
          background: linear-gradient(to bottom, #013842, 80%, #036574);
          border-top: 2px solid #067aae;
        }
        .titlehealth {
          font-size: 13px;
          font-family: "SimHei Regular";
          color: #a2d4e5;
          display: block;
          margin: 20px 0 0 25px;
        }
        .lintg {
          width: 100%;
          height: 225px;
        }
      }
      .grade {
        width: 254px;
        height: 251px;
        margin: 10px 0 0 40px;
        position: absolute;
        bottom: 50px;
        left: 0;
        img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
}
</style>