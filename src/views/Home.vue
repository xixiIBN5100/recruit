<template>
  <div style="display: flex; justify-content: center;margin-top: 20px;">
    <span style=" display: flex; gap: 15px; width: 90%">
      <el-input v-model="search" placeholder="查询企业" />
      <el-button type="primary" @click="handleSearch" >查询</el-button>
    </span>
  </div>

  <div style="display: flex; justify-content: center;margin-top: 20px;">
    <Card name="1" begin-time="123" state="123" place="123" recruit="123" link="123" introduce="123"></Card>
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
