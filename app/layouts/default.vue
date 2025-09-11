<template>
    <div class="default-layout min-h-screen w-full flex flex-col">
        <TheNavbar />
        <PageNavbar />

        <div class="flex-auto">
            <slot />
        </div>
    </div>
</template>

<script setup>
import TheNavbar from "@/components/layout/TheNavbar.vue";
import PageNavbar from "@/components/layout/PageNavbar.vue";
</script>

<style lang="postcss" scoped>

</style>