<script setup>
const { locale } = useI18n()

const urls = [
  {
    url: 'https://www-me777.com/',
    name: 'NCSC',
  },
  {
    url: 'https://www-me777.com/',
    name: 'NetSafe',
  },
  {
    url: 'https://www-me777.com/',
    name: 'Bitwarden',
  },
  {
    url: 'https://www-me777.com/',
    name: 'OwnYourOnline',
  },
  {
    url: (locale.value === 'ko') ? 'https://www-me777.com/' : 'https://www.www-me777.com/',
    name: 'Samsung',
  },
]

function getSvgIconUrl(name) {
  return `/images/home/${name.toLowerCase()}.svg`
}
</script>

<template>
  <div class="mt-20 h-[12vh] flex items-center justify-center">
    <ul class="flex flex-wrap list-none justify-center gap-12 px-8" role="list">
      <li v-for="link in urls" :key="link.name" role="listitem" class="flex">
        <NuxtLink
          :href="link.url"
          target="_blank"
          rel="noopener"
          :aria-label="link.label"
          class="group inline-block rounded focus:outline-none focus:ring-2 focus:ring-blue-500"
        >
          <div
            class="h-[40px] w-[128px] flex items-center justify-center p-4"
            style="aspect-ratio: 128 / 40"
          >
            <NuxtImg
              :src="getSvgIconUrl(link.name)"
              :alt="`${link.name} logo`"
              width="128"
              height="40"
              loading="lazy"
              class="h-auto max-h-16 max-w-[120px] brightness-0 invert-0 filter transition duration-300 ease-in-out group-hover:opacity-0 group-hover:opacity-75 dark:invert"
            />
          </div>
          <span class="sr-only">{{ link.name }}</span>
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<style scoped>
/* Add any additional styles here if needed */
</style>
