<script setup lang="ts">
definePageMeta({
  layout: 'home',
})

const online = useOnline()
</script>

<template>
  <div>
    <Logos mb-6 />
    <ClientOnly>
      <Suspense>
        <PageView v-if="online" />
        <div v-else text-gray:80>
          你似乎断开了与服务器的连接，但这也许不是你的问题。
        </div>
        <template #fallback>
          <div op50 italic>
            <span animate-pulse>正在玩命加载中...</span>
          </div>
        </template>
      </Suspense>
      <template #fallback>
        <div op50>
          <span animate-pulse>让我想想呢...</span>
        </div>
      </template>
    </ClientOnly>
    <Introduction />
  </div>
</template>
