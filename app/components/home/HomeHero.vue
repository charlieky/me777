<template>
  <header class="relative min-h-[120dvh] flex items-start justify-center overflow-hidden bg-white <sm:min-h-[90vh] dark:bg-black">
    <!-- SVG Graphic (Desktop Only) -->
    <div class="hidden md:(absolute inset-0 z-0 flex items-center justify-center)" aria-hidden="true">
      <UiSvg load-s-v-g="beta02" class="h-full w-full object-contain" />
    </div>
    <div class="relative z-20 mx-auto min-h-[55vh] w-full flex flex-col px5 sm:items-center sm:text-center">
      <!-- Vertical spacer -->
      <div class="flex-grow-1" />

      <!-- Content Group -->
      <div class="pt-10 md:pt-15">
        <!-- Reduced top padding -->
        <!-- Tagline -->

        <!-- Heading -->
        <h1 id="hero" class="m0 mb10 max-w-[90%] max-w-6xl w-full justify-center text-2xl 2xl:text-7xl lg:text-5xl md:text-4xl xl:text-6xl">
          {{ $t('v2.home.heroHeading') }}
        </h1>

        <div class="mx-auto mb4 flex items-center justify-center text-sm text-brand-light font-semibold uppercase space-x-2 md:text-lg dark:text-yellow-400">
          <Icon name="mdi:web" class="h6 w6 text-inherit" aria-hidden="true" />
          <span>{{ $t('v2.home.heroTagline') }}</span>
        </div>
        <!-- Subhead -->
        <p class="mx-auto mb-4 max-w-[90%] max-w-xl w-full text-xs text-neutral-600 2xl:text-xl lg:text-base md:text-sm xl:text-lg dark:text-neutral-300">
          {{ $t('v2.home.heroSubhead') }}
        </p>
      </div>

      <!-- CTA Button -->
      <NuxtLinkLocale
        class="mb-10 mt-10 flex items-center core-border border-brand-light rounded-full border-dashed core-theme px5 py1.5 text-center text-sm text-blue-6 no-underline transition duration-300 ease-in-out <sm:mr-auto md:mb-20 hover:(scale-110 border-solid) space-x-1 dark:border-yellow-3 md:text-base dark:text-yellow-4"
        to="/blog"
      >
        <span class="m0">{{ $t('v2.home.heroCta') }}</span>
        <Icon name="lucide:arrow-up-right" class="h5 w5" aria-hidden="true" />
      </NuxtLinkLocale>
    </div>

    <div class="pointer-events-none absolute inset-0 h-full w-full">
      <img
        src="/images/home/layer2.png"
        class="absolute bottom-0 z-0 h-[75vh] w-full object-bottom <sm:(h-[55vh] min-h-300px) md:h-3/4"
        alt="Base background texture"
        loading="lazy"
        decoding="async"
      >

      <img
        src="/images/home/layer.png"
        class="absolute inset-0 z-10 w-full"
        alt="Decorative foreground layer"
      >
    </div>
  </header>
</template>
