<script setup lang="ts">
import { RouterView } from 'vue-router'
import {ref} from "vue";
import router from "@/router";

const activeIndex = ref('1')
const handleSelect = (key: string) => {
activeIndex.value = key
}
</script>

<template>
  <el-menu
    class="el-menu-demo"
    mode="horizontal"
    :ellipsis="false"
    :default-active="activeIndex"
    @select="handleSelect"
  >
    <el-menu-item index="0">
      计算机学院就业信息表
    </el-menu-item>
    <el-menu-item index="1" @click="router.push('/')">企业总表</el-menu-item>
    <el-menu-item index="2">宣讲日历</el-menu-item>
  </el-menu>
  <RouterView />
</template>


<style scoped>
.el-menu--horizontal > .el-menu-item:nth-child(1) {
  margin-right: auto;
}
</style>
