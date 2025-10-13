<script lang="ts" setup>
import FooterItem from './Footer/FooterItem.vue'

const { t } = useI18n()
</script>

<template>
  <footer
    class="justify-center border-t-1 border-t-dark-4/10 border-solid border-b-none border-l-none border-r-none bg-inherit bg-white px-6 py-6 text-inherit dark:border-t-dark-2/30 dark:bg-black lg:px30 md:px-15 xl:px40"
  >
    <div class="flex flex-col items-start justify-between md:flex-row">
      <UiLogo class="h-auto w-24 text-gray-100" />

      <div class="grid grid-cols-2 mt-6 gap-8 md:mt-0 md:flex md:gap-12">
        <FooterItem
          :title="t('footer.community')"
          title-class="text-gray-300"
          :links="[{ text: t('footer.telegram'), href: 'https://t.me/+H2V-8z1VhxY0ODQ1', external: true }]"
          link-class="text-gray-400 hover:text-white transition-colors"
        />

        <FooterItem
          :title="t('footer.blog')"
          title-class="text-gray-300"
          :links="[{ text: t('footer.latest'), href: '/blog' }]"
          link-class="text-gray-400 hover:text-white transition-colors"
        />

        <FooterItem
          :title="t('footer.resources')"
          title-class="text-gray-300"
          :links="[{ text: t('footer.tools'), href: '/resources' }]"
          link-class="text-gray-400 hover:text-white transition-colors"
        />

        <FooterItem
          :title="t('footer.legal')"
          title-class="text-gray-300"
          :links="[
            { text: t('footer.privacy'), href: '/privacy-policy' },
            { text: t('footer.terms'), href: '/terms-of-service' },
          ]"
          link-class="text-gray-400 hover:text-white transition-colors"
        />
      </div>
    </div>

    <div class="mt-8 border-t border-gray-800 pt-6">
      <div class="flex flex-col items-start justify-between text-sm text-gray-400 md:flex-row">
        <p>{{ t('footer.copyright') }}</p>
      </div>
    </div>
  </footer>
</template>
