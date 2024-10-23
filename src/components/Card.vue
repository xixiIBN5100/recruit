<template>
  <div style="background-color: #e6e6e6; border-radius: 10px; min-width: 180px;flex: 1;cursor: pointer">
    <div style="display: flex; margin-top: 20px; padding: 0 15px;">
    <div style="font-size: 1rem;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;">
      {{ props.name }}
    </div>
    </div>
    <div style="padding: 10px">
    <div v-for="item in showDate" style="padding: 5px;font-size: 0.85rem;">
      <div>
        {{ item.context }}:
      </div>
      <div v-if="item.context === '宣讲状态' || item.context === '招聘状态'" style="margin-top: 5px;" >
        <el-tag>{{ item.content }}</el-tag>
      </div>
      <div v-else-if="item.context === '公司简介'" style="margin-top: 5px;overflow: hidden;text-overflow: ellipsis;display:-webkit-box; -webkit-box-orient:vertical; -webkit-line-clamp:3">
        {{ item.content }}
      </div>
      <div v-else style="overflow:hidden;text-overflow:ellipsis;white-space:nowrap;margin-top: 5px;">
        {{ item.content }}
      </div>
    </div>
    </div>
  </div>
</template>


<script setup lang="ts">
import {ref} from "vue";
const props = defineProps<{
  name: string,
  beginTime: string,
  state: string,
  recruitState: string,
  place: string,
  recruit: string,
  link: string,
  introduce: string,
}>()

const showDate = ref([
  {
    context: '宣讲状态',
    content: props.state
  },
  {
    context: '宣讲开始时间',
    content: props.beginTime
  },
  {
    context: '招聘状态',
    content: props.recruitState
  },
  {
    context: '宣讲地点',
    content: props.place
  },
  {
    context: '招聘岗位',
    content: props.recruit
  },
  {
    context: '网申链接',
    content: props.link
  },
  {
    context: '公司简介',
    content: props.introduce
  }
])
</script>


<style scoped>

</style>
