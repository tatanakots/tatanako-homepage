<script setup lang="ts">
const router = useRouter()
</script>

<template>
  <main p="x4 y10" text="center pink-400 dark:gray-200">
    <div text-4xl>
      <div i-carbon-warning inline-block />
    </div>
    <div>找不到页面诶</div>
    <div>
      <button text-sm btn m="3 t8" @click="router.back()">
        返回上一页
      </button>
    </div>
  </main>
</template>
