<template>
    <el-drawer v-model="visible" title="I am the title" :with-header="false" :size="isMobile ? '66%' : '20%'" class="overflow-y: auto">
        <div class="text-lg">{{props.name}}</div>
        <div class="text-md mt-5 text-blue-500">宣讲信息</div>
        <div class="ml-3">
            <div class="mt-3">
                <span class="text-sm">宣讲状态:</span> <br> <el-tag>{{props.state}}</el-tag> 
            </div>
            <div class="mt-1">
                <span class="text-sm">宣讲开始时间:</span> <br> <span class="text-sm">{{props.beginTime}}</span> 
            </div>
            <div class="mt-1">
                <span class="text-sm">宣讲地点:</span> <br> <span class="text-sm">{{props.place}}</span> 
            </div>
        </div>
        <div class="text-md mt-5 mt-5">招聘信息</div>
        <div class="ml-3">
            <div class="mt-3">
                <span class="text-sm ">招聘状态:</span> <br> <el-tag>{{props.recruitState}}</el-tag> 
            </div>
            <div class="mt-1">
                <span class="text-sm">
                    招聘岗位:
                </span> <br>    
                <span v-for="item in recruitArr">
                    <el-tag>{{item}}</el-tag> 
                </span>
            </div>
            <div class="mt-1">
                <span class="text-sm">网申地址: </span> <br>
                <a :href="props.link" class="text-sm underline" target="_blank">{{props.link}}</a>
            </div>
            <div class="mt-1">
                <span class="text-sm ">公司简介:</span> <br> {{props.introduce}}
            </div>
        </div>
    </el-drawer>
</template>


<script setup lang="ts">

import {ref, watch, computed} from "vue";

const props = defineProps<{
  modelValue: boolean,
  name: string,
  beginTime: string,
  state: string,
  recruitState: string,
  place: string,
  recruit: string,
  link: string,
  introduce: string,
}>()

const recruitArr = computed(
    () => {
        return props.recruit.split('、')
    }
)

const isMobile = computed(() => {
  return window.innerWidth <= 768;
});

const emit = defineEmits(['update:modelValue'])

const visible = ref(props.modelValue)

watch(() => props.modelValue, (newVal) => {
  visible.value = newVal;
});

watch(visible,(newVal) => {
    emit('update:modelValue',newVal)
})

</script>
