<template>
  <div>
    <div>
      {{ props.name }}
    </div>
    <div v-for="item in showDate">
      <div>
        {{ item.context }}
      </div>
      <div v-if="item.content === '宣讲状态' || item.content === '招聘状态'">
        <el-tag>{{ item.content }}</el-tag>
      </div>
      <div v-else>
        {{ item.content }}
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
