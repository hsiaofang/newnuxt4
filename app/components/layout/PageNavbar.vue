<template>
  <nav
    class="flex justify-center items-center sticky top-0 left-0 right-0 bg-[#5f6771ad] shadow-sm backdrop-blur-md z-50 px-2"
  >

    <!-- 導航選單 -->
    <ul class="flex flex-1 justify-center gap-2 m-0 p-0 items-center">
      <li class="list-none">
        <nuxt-link
          to="/"
          class="block px-4 py-4 text-[#e0e2e9] transition hover:text-white hover:bg-[#e0e2e91e]"
          exact-active-class="text-white bg-[#e0e2e91e]"
        >
          首頁
        </nuxt-link>
      </li>
      <li class="list-none">
        <nuxt-link
          to="/blogs"
          class="block px-4 py-4 text-[#e0e2e9] transition hover:text-white hover:bg-[#e0e2e91e]"
          exact-active-class="text-white bg-[#e0e2e91e]"
        >
          部落格
        </nuxt-link>
      </li>
      <li class="list-none">
        <nuxt-link
          to="/projects"
          class="block px-4 py-4 text-[#e0e2e9] transition hover:text-white hover:bg-[#e0e2e91e]"
          exact-active-class="text-white bg-[#e0e2e91e]"
        >
          作品集
        </nuxt-link>
      </li>
    </ul>

    <!-- 右側區塊 (桌機顯示) -->
    <div class="flex-1 max-md:hidden"></div>
  </nav>
</template>