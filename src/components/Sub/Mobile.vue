<template>
  <div>
    <el-row :gutter="20">
      <el-col :xs="24" :sm="24" :md="8" :lg="8" :xl="8">
        <div class="sub-wrapper">
          <div-header :header="'夏季预选赛和秋季预选赛'"></div-header>

          <button class="sub-title">
            比赛时间
          </button>
          <div class="sub-content">
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6月9日14:00-17:00
            </p>
          </div>
          <button class="sub-title">
            比赛内容
          </button>

          <div class="sub-content">
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;登录<a target="_blank"
                                                       :href="'http://www.mooctest.net/contest/list'">慕测平台</a>，报名<b>“2018年大学生移动应用测试大赛”</b>，直接采用慕测WebIDE或者下载安装<a
              target="_blank"
              :href="'http://www.mooctest.net/download'">Eclipse客户端</a>，在比赛前完成“我的任务”中的<b>“2018移动应用测试资格练习”</b>并达到规定分数。
            </p>
          </div>

          <button class="sub-title">
            评分标准
          </button>

          <div class="sub-content">
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. 预选赛发布两道题，每道题计算Appium脚本的测试需求对象覆盖率，即在需求范围内，覆盖对象数/总对象数*100，两道题相加得总分；
            </p>
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. 覆盖总分相同，则两道题测试脚本运行时间相加进行二次排序（短优先）；
            </p>
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. 运行时间相同，则按Appium脚本的运行稳定性进行三次排序。
            </p>
          </div>

          <button class="sub-title">
            注&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;意
          </button>
          <div class="sub-content">
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;移动应用测试大赛<b>A组（在校大学生）</b>、<b>B组（高职高专学生）</b>均可报名。
            </p>
          </div>

          <button class="sub-title">
            成绩公示
          </button>
          <div class="sub-content">
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;夏季预选赛<a :href="'http://mooctest.org/#/NewProgress'">成绩公示</a>与资格查询:
            </p>
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<i class="el-icon-download"></i> <a
              :href="SummerMobilePUrl">夏季预选赛移动应用测试（个人）</a>
            </p>
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<i class="el-icon-download"></i> <a
              :href="SummerMobileGUrl">夏季预选赛移动应用测试（团队）</a>
            </p>
          </div>
        </div>
      </el-col>
      <el-col :xs="24" :sm="24" :md="8" :lg="8" :xl="8">
        <div class="sub-wrapper">
          <div-header :header="'省区赛'"></div-header>

          <button class="sub-title">
            比赛内容
          </button>

          <div class="sub-content">
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;组委会提供来自企业的待测移动应用和测试需求，在慕测的WebIDE或者<a
              target="_blank"
              :href="'http://www.mooctest.net/download'">Eclipse客户端</a>完成Appium测试脚本。
            </p>
          </div>

          <button class="sub-title">
            评分标准
          </button>

          <div class="sub-content">
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. 省区赛发布两道题，每道题计算Appium脚本的测试需求对象覆盖率，即在需求范围内，覆盖对象数/总对象数*100，两道题相加得总分；
            </p>
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. 覆盖总分相同，则两道题测试脚本运行时间相加进行二次排序（短优先）；
            </p>
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. 运行时间相同，则按Appium脚本的运行稳定性进行三次排序。
            </p>
          </div>
        </div>
      </el-col>
      <el-col :xs="24" :sm="24" :md="8" :lg="8" :xl="8">
        <div class="sub-wrapper">
          <div-header :header="'总决赛'"></div-header>
          <button class="sub-title">
            比赛内容
          </button>

          <div class="sub-content">
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;组委会提供来自企业的待测移动应用和测试需求，在慕测的WebIDE或者<a
              target="_blank"
              :href="'http://www.mooctest.net/download'">Eclipse客户端</a>完成Appium测试脚本，在慕测平台完成众包测试。
            </p>
          </div>

          <button class="sub-title">
            评分标准
          </button>

          <div class="sub-content">
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. 评分标准1：Appium脚本的测试需求覆盖率；
            </p>
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. 评分标准2：众包测试的Bug检测率，具体参阅题目要求；
            </p>
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. 评分标准1和2加权累计得该题分数，具体参阅题目要求；
            </p>
            <p>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. 总分相同的选手按Appium脚本运行时间二次排名，短则优。
            </p>
          </div>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>

  import DivHeader from '../Util/DivHeader.vue'
  import {Col, Row} from 'element-ui'
  import {router} from '../../main'

  import SummerMobileGPdf from '../../assets/pdf/summer-mobile-g.pdf'
  import SummerMobilePPdf from '../../assets/pdf/summer-mobile-p.pdf'

  export default {
    name: 'mobile',
    components: {
      DivHeader,
      elCol: Col,
      elRow: Row,
      SummerMobileGPdf,
      SummerMobilePPdf,
    },
    data() {
      return {
        SummerMobileGUrl: SummerMobileGPdf,
        SummerMobilePUrl: SummerMobilePPdf,
      }
    },
    methods: {}
  }
</script>

<style scoped src="./Sub.css"></style>
