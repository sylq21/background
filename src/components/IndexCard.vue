<template>
    <el-card shadow="never">
        <template #header>
            <div class="flex justify-between">
                <span class="text-sm">{{ title }}</span>
                <el-tag effect = "plain" type="danger">
                    {{ tip }}
                </el-tag>
            </div>
        </template>
        <el-row :gutter = "20">
            <el-col :span="6" :offset="0" v-for="(item,index) in btns" :key="index">
                <el-card :shadow="hover" class="border-0 bg-light-4000">
                    <div class="flex flex-col items-center justify-center">
                        <span class="text-xl mb-2">{{ item.value }}</span>
                        <span class="text-xs">{{ item.label }}</span>
                    </div>
                </el-card>
            </el-col>
        </el-row>
    </el-card>
</template>

<script setup>
defineProps({
    title:String,
    tip:String,
    btns:Array
})

</script>