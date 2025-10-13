<script setup lang="ts">
const head = useLocaleHead({
  dir: true,
  seo: true,
})

useSeoMeta({
  titleTemplate: '%s - Xanzhu',
})
</script>

<template>
  <Html v-if="head.htmlAttrs" :lang="head.htmlAttrs.lang" class="scroll-pt-[73px] antialiased">
    <Head>
      <template v-for="link in head.link" :key="link.id">
        <Link :id="link.id" :rel="link.rel" :href="link.href" :hreflang="link.hreflang" />
      </template>
      <template v-for="meta in head.meta" :key="meta.id">
        <Meta :id="meta.id" :property="meta.property" :content="meta.content" />
      </template>
    </Head>
    <Body class="m0 core-theme font-sans">
      <AppHeader class="sticky top-0 z-20" />
      <UiInfoBar />
      <NuxtPage />
      <LazyAppFooter />

      <div class="fixed right-4 top-1/2 z-[70] flex flex-col transform gap-3 -translate-y-1/2">
        <a
          href="https://t.me/+H2V-8z1VhxY0ODQ1"
          target="_blank"
          rel="noopener"
          class="group rounded-full bg-[#0088cc] p-4 shadow-xl transition-all duration-300 hover:scale-125"
          aria-label="Telegram"
        >
          <svg class="h-8 w-8 text-white" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm5.894 8.221l-1.97 9.28c-.145.658-.537.818-1.084.508l-3-2.21-1.446 1.394c-.14.14-.26.26-.514.26l.2-3.005 5.594-5.04c.24-.213-.054-.334-.373-.121l-6.97 4.48-3.02-.94c-.64-.203-.658-.64.136-.954l11.7-4.5c.534-.196 1.002.13.832.941z" />
          </svg>
          <span class="absolute right-full top-1/2 mr-2 rounded-lg bg-gray-800 px-3 py-2 text-base text-white opacity-0 transition-opacity -translate-y-1/2 group-hover:opacity-100">
            Join Telegram
          </span>
        </a>
      </div>

      <UiScrollButton />
    </Body>
  </Html>
</template>
