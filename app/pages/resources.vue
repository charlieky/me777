<script setup lang="ts">
interface Link {
  name: string
  url: string
  description: string
}

interface Resource {
  id: string
  title: string
  fullDescription: string
  icon: string
  links: Link[]
  reporting: Link[]
}

const { t } = useI18n()
const resources = ref<Resource[]>([
  {
    id: '01',
    title: t('resources.phishing'),
    fullDescription: t('resources.explain.phishing'),
    icon: 'ri-gift-fill',
    links: [
      {
        name: 'License',
        url: 'https://www-me777.com/',
        description: t('resources.tools.License'),
      },
      {
        name: 'Reputation',
        url: 'https://www-me777.com/',
        description: t('resources.tools.Reputation'),
      },
      {
        name: 'MarketPosition',
        url: 'https://www-me777.com/',
        description: t('resources.tools.MarketPosition'),
      },
      {
        name: 'Products',
        url: 'https://www-me777.com/',
        description: t('resources.tools.Products'),
      },
    ],
    reporting: [
      {
        name: 'Services',
        url: 'https://www-me777.com',
        description: t('resources.reporting.Services'),
      },

    ],
  },
  {
    id: '02',
    title: t('resources.malware'),
    fullDescription: t('resources.explain.malware'),
    icon: 'ri-loop-right-line',
    links: [
      {
        name: 'Membership-Day-8th',
        url: 'https://www-me777.com',
        description: t('resources.tools.Membership-Day-8th'),
      },
      {
        name: 'Membership-Day-18th',
        url: 'https://www-me777.com',
        description: t('resources.tools.Membership-Day-18th'),
      },
      {
        name: 'Membership-Day-28th',
        url: 'https://www-me777.com',
        description: t('resources.tools.Membership-Day-28th'),
      },
      {
        name: 'Rewards',
        url: 'https://www-me777.com',
        description: t('resources.tools.Rewards'),
      },
    ],
    reporting: [
      {
        name: 'Notification',
        url: 'https://www-me777.com',
        description: t('resources.reporting.Notification'),
      },

    ],
  },

])

const searchQuery = ref<string>('')
const filteredResources = computed(() => {
  const query = searchQuery.value.toLowerCase()
  return !query
    ? resources.value
    : resources.value
        .map(resource => ({
          ...resource,
          links: resource.links.filter(
            link =>
              link.name.toLowerCase().includes(query)
              || link.description.toLowerCase().includes(query),
          ),
          reporting: resource.reporting.filter(
            tool =>
              tool.name.toLowerCase().includes(query)
              || tool.description.toLowerCase().includes(query),
          ),
        }))
        .filter(
          resource =>
            resource.links.length > 0
            || resource.reporting.length > 0
            || resource.title.toLowerCase().includes(query)
            || resource.fullDescription.toLowerCase().includes(query),
        )
})

const seoImage = 'https://images.pexels.com/photos/27206011/pexels-photo-27206011.jpeg'
useLangMeta('resources.meta', seoImage)
</script>

<template>
  <div class="min-h-screen core-ui bg-gradient-to-b">
    <div class="relative">
      <div class="absolute inset-0 overflow-hidden">
        <NuxtImg
          src="https://res.cloudinary.com/dtvdfo5yq/image/upload/v1760240317/layer_xles2c.png" alt="Hero Background" class="h-auto w-full object-cover"
          height="auto" width="800" loading="eager" fetchpriority="high"
          sizes="(max-width: 640px) 100vw, (max-width: 1024px) 50vw, 800px"
        />
      </div>
      <div class="relative mx-auto max-w-7xl px-4 py-24 text-center">
        <div class="inline-block rounded-xl bg-white p-8 dark:bg-black">
          <h1 class="mb-6 min-h-50px text-4xl text-gray-800 font-bold md:text-5xl dark:text-gray-100">
            {{ t('resources.hero.title') }}
          </h1>
          <p class="mx-auto max-w-2xl text-lg text-gray-700 font-400 opacity-90 dark:text-gray-300">
            {{ t('resources.hero.description') }}
          </p>
        </div>
      </div>
    </div>
    <div class="mx-auto max-w-4xl px-4 -mt-8">
      <div class="p-2">
        <div class="relative flex items-center text-inherit">
          <Icon name="ri:search-line" class="absolute left-3 h-5 w-5 text-gray-3" aria-hidden="true" />
          <input
            v-model="searchQuery" type="text" :placeholder="t('resources.search.placeholder')"
            :aria-label="t('resources.search.placeholder')" role="searchbox"
            class="w-full rounded-lg border-none bg-white p4 pl-10 pr-4 text-16px text-dark1 dark:bg-black dark:text-white focus:outline-none focus:ring-none"
          >
        </div>
        <div v-if="!filteredResources.length" class="mt-4 text-center text-dark1 dark:text-white">
          {{ t('resources.search.noResults') }}
        </div>
      </div>
    </div>
    <div
      v-if="filteredResources.length && filteredResources.some(resource => resource.links.length || resource.reporting.length)"
      class="mx-auto max-w-4xl p4 pb15% space-y-12"
    >
      <div v-for="resource in filteredResources" :key="resource.id" class="space-y-4">
        <div v-if="resource.links.length || resource.reporting.length" class="flex items-center space-x-2">
          <Icon
            v-if="resource.icon" :name="resource.icon" class="h6 w-auto text-black dark:text-white"
            aria-hidden="true"
          />
          <h2 class="m0 text-2xl text-gray-800 font-semibold dark:text-gray-100">
            {{ resource.title }}
          </h2>
        </div>
        <p v-if="resource.links.length || resource.reporting.length" class="m0 text-gray-600 dark:text-gray-300">
          {{
            resource.fullDescription }}
        </p>
        <ul v-if="resource.links.length" class="space-y-2">
          <li v-for="link in resource.links" :key="link.name">
            <NuxtLink
              :href="link.url" target="_blank" rel="noopener noreferrer"
              class="text-inherit underline underline-offset-2 hover:text-brand-light dark:hover:text-brand-dark"
            >
              {{ link.name }}
            </NuxtLink>
            <span class="text-gray-600 dark:text-gray-400"> - {{ link.description }}</span>
          </li>
        </ul>
        <ul v-if="resource.reporting.length" class="mt-4 space-y-2">
          <li v-for="tool in resource.reporting" :key="tool.name">
            <NuxtLink
              :href="tool.url" target="_blank" rel="noopener noreferrer"
              class="text-inherit underline underline-offset-2 hover:text-brand-light dark:hover:text-brand-dark"
            >
              {{ tool.name }}
            </NuxtLink>
            <span class="text-gray-600 dark:text-gray-400"> - {{ tool.description }}</span>
          </li>
        </ul>
      </div>

      <NuxtImg
        src="https://res.cloudinary.com/dtvdfo5yq/image/upload/v1760266313/member_het6y8.png" alt="Hero Background" class="h-auto w-full object-cover"
        height="auto" width="800" loading="eager" fetchpriority="high"
        sizes="(max-width: 640px) 100vw, (max-width: 1024px) 50vw, 800px"
      />
    </div>
  </div>
</template>
