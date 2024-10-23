<template>
  <div style="display: flex; justify-content: center;margin-top: 20px;">
    <span style=" display: flex; gap: 15px; width: 90%">
      <el-input v-model="search" placeholder="查询企业" />
      <el-button type="primary" @click="handleSearch" >查询</el-button>
    </span>
  </div>

  <div style="display: flex; justify-content: start;margin-top: 20px; gap: 10px; flex-flow: wrap; width: auto; margin-left: 20px;margin-right: 20px;">
    <Card name="杭州士兰微电子股份有限公司" begin-time="2024/10/23 14:00" state="即将开始" place="屏峰校区广知楼B512" recruit="MEMS 产品工程师、器件产品工程师、IPM 系统应用工程师、AE工程师等" link="https://zjut.jysd.com/teachin/view/id/176543" introduce="杭州士兰微电子股份有限公司（600460）坐落于杭州高新技术产业开发区，是专业从事集成电路芯片设计 以及半导体微 电子相关产品生产的高新技术企业。是第一家在中国境内上市的集成电路芯片设计企业。公司的技术与产品涵盖了众多领域，在多个技术领域保持了国内领先的地位" recruit-state="正在招聘"></Card>
    <Card name="杭州士兰微电子股份有限公司" begin-time="2024/10/23 14:00" state="即将开始" place="屏峰校区广知楼B512" recruit="MEMS 产品工程师、器件产品工程师、IPM 系统应用工程师、AE工程师等" link="https://zjut.jysd.com/teachin/view/id/176543" introduce="杭州士兰微电子股份有限公司（600460）坐落于杭州高新技术产业开发区，是专业从事集成电路芯片设计 以及半导体微 电子相关产品生产的高新技术企业。是第一家在中国境内上市的集成电路芯片设计企业。公司的技术与产品涵盖了众多领域，在多个技术领域保持了国内领先的地位" recruit-state="正在招聘"></Card>
    <Card name="杭州士兰微电子股份有限公司" begin-time="2024/10/23 14:00" state="即将开始" place="屏峰校区广知楼B512" recruit="MEMS 产品工程师、器件产品工程师、IPM 系统应用工程师、AE工程师等" link="https://zjut.jysd.com/teachin/view/id/176543" introduce="杭州士兰微电子股份有限公司（600460）坐落于杭州高新技术产业开发区，是专业从事集成电路芯片设计 以及半导体微 电子相关产品生产的高新技术企业。是第一家在中国境内上市的集成电路芯片设计企业。公司的技术与产品涵盖了众多领域，在多个技术领域保持了国内领先的地位" recruit-state="正在招聘"></Card>
    <Card name="杭州士兰微电子股份有限公司" begin-time="2024/10/23 14:00" state="即将开始" place="屏峰校区广知楼B512" recruit="MEMS 产品工程师、器件产品工程师、IPM 系统应用工程师、AE工程师等" link="https://zjut.jysd.com/teachin/view/id/176543" introduce="杭州士兰微电子股份有限公司（600460）坐落于杭州高新技术产业开发区，是专业从事集成电路芯片设计 以及半导体微 电子相关产品生产的高新技术企业。是第一家在中国境内上市的集成电路芯片设计企业。公司的技术与产品涵盖了众多领域，在多个技术领域保持了国内领先的地位" recruit-state="正在招聘"></Card>

  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Card from "@/components/Card.vue";

const search = ref('')

const handleSearch = () => {
  console.log(search.value)
}
</script>
