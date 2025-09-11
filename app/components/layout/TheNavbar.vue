<template>
  <nav class="flex items-center justify-end py-4 px-6 border dark:border-gray-500">
    <div class="flex items-center gap-4">
      <client-only>
        <button
          class="flex px-2 py-1 rounded-md hover:bg-gray-200 dark:hover:bg-gray-700"
          @click="toggleDark()"
        >
          <svg
            v-if="isDark"
            class="h-7 w-7 p-1"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z"
            />
          </svg>
          <svg
            v-else
            class="h-7 w-7 p-1"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z"
            />
          </svg>
        </button>
      </client-only>
      <a
        href="https://github.com/你的GitHub帳號"
        target="_blank"
        rel="noopener noreferrer"
        class="hover:text-gray-600 dark:hover:text-gray-300"
      >
        <Github class="h-7 w-7" />
      </a>
    </div>
  </nav>
</template>

<script setup>
import { Github } from "lucide-vue-next";

const isDark = useDark();
const toggleDark = useToggle(isDark);
</script>
