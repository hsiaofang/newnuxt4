<template>
  <div class="index min-h-[calc(100vh-8.3rem)] flex flex-col items-center px-6 py-12">

    <!-- Hero Section -->
    <section class="text-center max-w-2xl">
      <h1 class="text-4xl font-bold mb-4">嗨，我是 <span class="text-blue-500">Zoe</span> 👋</h1>
      <p class="text-lg text-gray-600 dark:text-gray-300">
        這裡是我的作品集，展示了我在前端、後端與全端開發上的實戰經驗。
      </p>
    </section>

    <!-- Works Section -->
    <section class="mt-12 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 w-full max-w-6xl">
      <Card v-for="(work, i) in works" :key="i" class="hover:shadow-lg transition-shadow">
        <CardHeader>
          <img :src="work.image" alt="work preview" class="rounded-xl mb-2 h-40 w-full object-cover" />
          <CardTitle class="text-xl font-semibold">{{ work.title }}</CardTitle>
        </CardHeader>
        <CardContent class="text-gray-600 dark:text-gray-300">
          {{ work.description }}
        </CardContent>
        <CardFooter>
          <Button as="a" :href="work.link" target="_blank" class="w-full">
            查看作品
          </Button>
        </CardFooter>
      </Card>
    </section>

    <!-- Info Section -->
    <ClientOnly>
      <HoverCard>
        <HoverCardTrigger>
          <Button class="mt-8 rounded-full h-8 w-8 p-0">
            <InfoCircledIcon class="rounded-full h-6 w-6" />
          </Button>
        </HoverCardTrigger>
        <HoverCardContent class="text-center">
          本網站使用 <strong>Nuxt 3</strong>, <strong>TailwindCSS</strong>, <strong>shadcn-vue</strong> 打造 ✨
        </HoverCardContent>
      </HoverCard>
    </ClientOnly>

  </div>
</template>

<script setup>
import { InfoCircledIcon } from '@radix-icons/vue'
import {
  HoverCard,
  HoverCardContent,
  HoverCardTrigger,
} from '@/components/ui/hover-card'
import {
  Card,
  CardHeader,
  CardTitle,
  CardContent,
  CardFooter
} from '@/components/ui/card'
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
