<template>
  <div class="index min-h-[calc(100vh-8.3rem)] flex flex-col items-center px-6 py-12 bg-gradient-to-b from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800 transition-colors">

    <!-- Hero Section -->
    <section class="text-center max-w-3xl">
      <h1 class="text-5xl md:text-6xl font-extrabold mb-4 text-gray-900 dark:text-white">
        嗨，我是 <span class="text-blue-500">Zoe</span> 👋
      </h1>
      <p class="text-lg md:text-xl text-gray-600 dark:text-gray-300 mt-2">
        這裡是我的作品集，展示我在前端、後端與全端開發上的實戰經驗。
      </p>
    </section>

    <!-- Works Section -->
    <section class="mt-16 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 w-full max-w-7xl">
      <ProjectCard v-for="(work, i) in works" :key="i" :project="work" />
    </section>

    <!-- Info Section -->
    <ClientOnly>
      <HoverCard class="mt-12">
        <HoverCardTrigger>
          <Button class="rounded-full h-12 w-12 p-0 flex items-center justify-center bg-gray-200 dark:bg-gray-700 hover:bg-gray-300 dark:hover:bg-gray-600 transition-colors shadow-md hover:shadow-lg">
            <InfoCircledIcon class="h-6 w-6 text-gray-700 dark:text-gray-200" />
          </Button>
        </HoverCardTrigger>
        <HoverCardContent class="text-center p-4 rounded-lg shadow-lg bg-white dark:bg-gray-800 text-gray-900 dark:text-gray-200">
          本網站使用 <strong>Nuxt 3</strong>, <strong>TailwindCSS</strong>, <strong>shadcn-vue</strong> 打造 ✨
        </HoverCardContent>
      </HoverCard>
    </ClientOnly>

  </div>
</template>

<script setup>
import { InfoCircledIcon } from '@radix-icons/vue'
import { HoverCard, HoverCardContent, HoverCardTrigger } from '@/components/ui/hover-card'
import { Button } from '@/components/ui/button'

const works = [
  {
    title: '產品管理系統',
    description: '支援產品 CRUD、圖片上傳、Excel 匯入與 QR Code 生成。',
    image: 'https://via.placeholder.com/400x200',
    link: '#'
  },
  {
    title: '訂單管理系統',
    description: '可新增、編輯、刪除訂單，並支援 Excel 匯入與批次列印。',
    image: 'https://via.placeholder.com/400x200',
    link: '#'
  },
  {
    title: 'CRM + LINE OA 整合',
    description: '整合 LINE 官方帳號與 CRM，自動派單與會員管理。',
    image: 'https://via.placeholder.com/400x200',
    link: '#'
  }
]
</script>
