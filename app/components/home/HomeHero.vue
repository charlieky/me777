<template>
  <header class="relative min-h-screen flex items-center justify-center bg-white dark:bg-black">
    <div class="hidden md:(absolute inset-0 z-0 flex items-center justify-center)" aria-hidden="true">
      <UiSvg load-s-v-g="beta02" class="h-100% w-full object-cover" />
    </div>

    <div
      class="relative z-10 mx-auto flex flex-col px5 py10 sm:items-center sm:text-center"
    >
      <div
        class="mb2 flex items-center text-sm text-brand-light font-semibold uppercase space-x-2 dark:text-yellow-400"
        role="doc-subtitle"
      >
        <Icon name="mdi:web" class="h6 w6 text-inherit" aria-hidden="true" />

        <span>{{ $t('v2.home.heroTagline') }}</span>
      </div>
      <h1 id="hero" class="m0 mb2 max-w-[90%] max-w-4xl w-full text-5xl md:text-7xl">
        {{ $t('v2.home.heroHeading') }}
      </h1>
      <p class="mx-auto mb-4 max-w-[90%] max-w-lg w-full text-sm text-neutral-600 md:text-lg dark:text-neutral-300">
        {{ $t('v2.home.heroSubhead') }}
      </p>
      <NuxtLinkLocale
        class="m25 mt5 flex items-center core-border border-brand-light rounded-full border-dashed core-theme px5 py1.5 text-center text-blue-6 no-underline transition duration-300 ease-in-out <sm:mr-auto hover:(scale-110 border-solid) space-x-1 dark:border-yellow-3 dark:text-yellow-4"
        to="/blog"
      >
        <span class="m0">
          {{ $t('v2.home.heroCta') }}
        </span>
        <Icon name="lucide:arrow-up-right" class="h5 w5" aria-hidden="true" />
      </NuxtLinkLocale>
    </div>

    <!-- Updated image code -->
    <img
      src="/images/home/layer.png"
      class="absolute bottom-17 z-0 h-auto w-full object-cover"
      alt="Decorative layer"
    >
  </header>
</template>
