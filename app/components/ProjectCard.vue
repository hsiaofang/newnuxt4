<template>
  <HoverCard>
    <HoverCardTrigger>
      <Card class="group hover:shadow-2xl transition-shadow duration-300 bg-white dark:bg-gray-900 rounded-2xl overflow-hidden border border-gray-200 dark:border-gray-700">
        <CardHeader class="p-0">
          <div class="relative overflow-hidden h-48 w-full">
            <img
              :src="project.image"
              :alt="project.title"
              class="rounded-t-2xl w-full h-full object-cover transform group-hover:scale-105 transition-transform duration-300"
            />
          </div>
          <CardTitle class="text-xl font-semibold p-4 pb-2 text-gray-900 dark:text-white">
            {{ project.title }}
          </CardTitle>
        </CardHeader>
        <CardContent class="text-gray-600 dark:text-gray-300 px-4 pb-4">
          {{ project.description }}
        </CardContent>
        <CardFooter class="px-4 pb-4">
          <Button
            as="a"
            :href="project.link"
            target="_blank"
            class="w-full bg-blue-500 hover:bg-blue-600 text-white font-medium shadow-md hover:shadow-lg transition-all duration-200 rounded-lg"
          >
            查看作品
          </Button>
        </CardFooter>
      </Card>
    </HoverCardTrigger>
    <HoverCardContent class="text-center p-4 rounded-lg shadow-lg bg-white dark:bg-gray-800 text-gray-900 dark:text-gray-200">
      本作品使用 <strong>Nuxt 3</strong>, <strong>TailwindCSS</strong>, <strong>shadcn-vue</strong> 打造 ✨
    </HoverCardContent>
  </HoverCard>
</template>

<script setup>
import { HoverCard, HoverCardTrigger, HoverCardContent } from '@/components/ui/hover-card'
import { Card, CardHeader, CardTitle, CardContent, CardFooter } from '@/components/ui/card'
import { Button } from '@/components/ui/button'

const props = defineProps({
  project: {
    type: Object,
    required: true
  }
})
</script>
