<script setup lang="ts">
import { useHead } from "@vueuse/head";

useHead({
  title: "Binh",
  meta: [
    { property: "og:title", content: "Binh" },
    { property: "og:image", content: "/avatar.jpg" },
    { property: "og:type", content: "website" },
  ],
  htmlAttrs: {
    // @ts-ignore - missing this html attribute in @vueuse/head
    prefix: "og: http://ogp.me/ns#",
  },
});

// @unocss-safelist: bg-sky-400 bg-op-70 fixed z-1031 top-0 inset-x-0 h-2px
</script>

<template>
  <Header />
  <main class="pt-$header-height">
    <div class="px-6 py-10 md:py-16">
      <router-view v-slot="{ Component }">
        <transition name="fade" mode="out-in">
          <component :is="Component" />
        </transition>
      </router-view>
    </div>
  </main>
  <Footer />
</template>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
