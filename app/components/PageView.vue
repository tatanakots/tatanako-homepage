<script setup lang="ts">
import { computed } from 'vue'
import { useFetch } from '#imports'
import { format, register } from 'timeago.js'
import zh_CN from 'timeago.js/lib/lang/zh_CN'

// 注册中文语言包
register('zh_CN', zh_CN)

const { data } = await useFetch('/api/pageview')

// 当 data.value.startAt 存在时，计算中文的时间描述
const timeAgo = computed(() => {
  if (!data.value?.startAt) return ''
  return format(data.value.startAt, 'zh_CN')
})
</script>

<template>
  <div text-gray:80>
    本页面自
    <span text-gray>{{ timeAgo }}</span>
    创建以来，已经被访问过
    <span text-gray font-500>{{ data?.pageview }}</span>
    次了。
  </div>
</template>
