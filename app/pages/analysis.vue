<script setup>
const seoImage = 'https://images.pexels.com/photos/27141316/pexels-photo-27141316.jpeg'
useLangMeta('analysis.meta', seoImage)
</script>

<template>
  <div class="min-h-screen bg-white dark:bg-black">
    <!-- Header Section -->
    <div class="text-center text-inherit">
      <h1 class="mb-2 text-4xl font-bold">
        {{ $t('analysis.hero.title') }}
      </h1>
      <p class="mx-auto max-w-2xl text-lg">
        {{ $t('analysis.hero.subhead') }}
      </p>
    </div>

    <!-- Key Trend Section -->
    <div class="mx-auto max-w-4xl px-4 py-12 space-y-12">
      <div class="core-border rounded-lg bg-white p-6 shadow-lg">
        <h2 class="mb-4 text-2xl text-gray-800 font-semibold">
          {{ $t('analysis.keyTrend.title') }}
        </h2>
        <p class="mb-6 text-gray-700">
          {{ $t('analysis.keyTrend.desc') }}
        </p>
        <h2 class="mb-4 text-2xl text-gray-800 font-semibold">
          {{ $t('analysis.keyTrend.title1') }}
        </h2>
        <div class="core-border rounded-lg bg-white p-6 shadow-lg">
          <h2 class="mb-4 text-2xl text-gray-800 font-semibold">
            {{ $t('analysis.keyTrend.title2') }}
          </h2>

          <div class="text-gray-700 space-y-3">
            <div class="commission-grid">
              {{ $t('analysis.keyTrend.desc2') }}
              <span class="text-emerald-600 font-bold">0.45%</span>
            </div>

            <div class="commission-grid">
              {{ $t('analysis.keyTrend.desc3') }}

              <span>0.3%</span>
            </div>

            <div class="commission-grid">
              {{ $t('analysis.keyTrend.desc4') }}

              <span>0.1%</span>
            </div>

            <div class="commission-grid">
              {{ $t('analysis.keyTrend.desc5') }}
              <span>0.05%</span>
            </div>
          </div>

          <p class="mt-2 border-t pt-4 text-gray-700">
            <span class="font-semibold"> {{ $t('analysis.keyTrend.title3') }}</span>
            {{ $t('analysis.keyTrend.desc6') }}
          </p>
        </div>

        <h2 class="text-2xl text-gray-800 font-semibold">
          {{ $t('analysis.keyTrend.title4') }}
        </h2>
        <p class="text-gray-700">
          {{ $t('analysis.keyTrend.desc7') }}
        </p>

        <div class="core-border rounded-lg bg-white p-6 shadow-lg">
          <div class="text-gray-700 space-y-3">
            <div class="commission-grid">
              <span>{{ $t('analysis.keyTrend.desc8') }}</span>
              <span class="text-emerald-600">{{ $t('analysis.keyTrend.desc9') }}</span>
            </div>
            <div class="commission-grid">
              <span>{{ $t('analysis.keyTrend.desc10') }}</span>
              <span class="text-emerald-600">{{ $t('analysis.keyTrend.desc11') }}</span>
            </div>
          </div>
        </div>

        <h2 class="text-2xl text-gray-800 font-semibold">
          {{ $t('analysis.keyTrend.title5') }}
        </h2>
        <p class="text-gray-700">
          {{ $t('analysis.keyTrend.desc12') }}
        </p>

        <div class="core-border rounded-lg bg-white p-6 shadow-lg">
          <div class="text-gray-700 space-y-3">
            <div class="commission-grid">
              <span> {{ $t('analysis.keyTrend.desc13') }}</span>
              <span class="text-emerald-600">{{ $t('analysis.keyTrend.desc14') }}</span>
            </div>
            <div class="commission-grid">
              <span> {{ $t('analysis.keyTrend.desc15') }}</span>
              <span class="text-emerald-600">{{ $t('analysis.keyTrend.desc16') }}</span>
            </div>
          </div>

          <p class="mt-2 border-t pt-4 text-gray-700">
            <span class="font-semibold"> {{ $t('analysis.keyTrend.title6') }}</span>
            {{ $t('analysis.keyTrend.desc17') }}
          </p>
        </div>
      </div>

      <div class="min-h-screen bg-white dark:bg-black">
        <!-- Header Section -->
        <div class="text-center text-inherit">
          <h1 class="text-4xl font-bold">
            {{ $t('analysis.hero.title1') }}
          </h1>
        </div>
        <div class="min-h-screen bg-white dark:bg-black">
          <!-- Header Section -->
          <div class="text-center text-inherit">
            <p class="mx-auto max-w-2xl text-lg">
              {{ $t('analysis.hero.title2') }}
            </p>
          </div>

          <!-- Benefits Section -->
          <div class="mx-auto max-w-4xl px-4 py-4 space-y-12">
            <!-- Referral System -->
            <div class="core-border rounded-lg bg-white p-6 shadow-lg">
              <h2 class="mb-4 text-2xl text-gray-800 font-semibold">
                1. {{ $t('analysis.hero.title3') }}
              </h2>
              <div class="commission-grid">
                <span class="text-gray-600"> {{ $t('analysis.hero.title4') }}</span>
                <span class="font-semi-bold text-emerald-600">{{ $t('analysis.hero.title5') }}</span>
              </div>
              <div class="commission-grid mt-2">
                <span class="text-gray-600">{{ $t('analysis.hero.title6') }}</span>
                <span class="text-emerald-600 font-bold">{{ $t('analysis.hero.title7') }}</span>
              </div>
            </div>

            <!-- Promotion Channels -->
            <div class="core-border rounded-lg bg-white p-6 shadow-lg">
              <h2 class="mb-4 text-2xl text-gray-800 font-semibold">
                2. {{ $t('analysis.hero.promotionTitle') }}
              </h2>
              <div class="grid grid-cols-2 gap-4 text-gray-700 md:grid-cols-3">
                <div class="flex items-center gap-2">
                  <span class="text-emerald-600">•</span> Facebook
                </div>
                <div class="flex items-center gap-2">
                  <span class="text-emerald-600">•</span> YouTube
                </div>
                <div class="flex items-center gap-2">
                  <span class="text-emerald-600">•</span> Telegram
                </div>
                <div class="flex items-center gap-2">
                  <span class="text-emerald-600">•</span> TikTok
                </div>
                <div class="flex items-center gap-2">
                  <span class="text-emerald-600">•</span> Skype
                </div>
                <div class="flex items-center gap-2">
                  <span class="text-emerald-600">•</span> Instagram
                </div>
              </div>
            </div>

            <!-- Commission Structure -->
            <div class="core-border rounded-lg bg-white p-6 shadow-lg">
              <h2 class="mb-4 text-2xl text-gray-800 font-semibold">
                3. {{ $t('analysis.hero.commissionTitle') }}
              </h2>
              <div class="text-gray-700 space-y-4">
                <div class="commission-grid">
                  <span> {{ $t('analysis.hero.title8') }}</span>
                  <span class="text-emerald-600">{{ $t('analysis.hero.title9') }}</span>
                </div>
                <div class="commission-grid">
                  <span>{{ $t('analysis.hero.title10') }}</span>
                  <span class="text-emerald-600">{{ $t('analysis.hero.title11') }}</span>
                </div>
                <div class="commission-grid">
                  <span>{{ $t('analysis.hero.title12') }}</span>
                  <span class="text-emerald-600">{{ $t('analysis.hero.title13') }}</span>
                </div>
                <div class="commission-grid">
                  <span>{{ $t('analysis.hero.title14') }}</span>
                  <span class="text-emerald-600">{{ $t('analysis.hero.title15') }}</span>
                </div>
              </div>
            </div>

            <NuxtImg
              src="https://res.cloudinary.com/dtvdfo5yq/image/upload/v1760247573/Agent_hh9akn.png" alt="Hero Background" class="h-auto w-full object-cover"
              height="auto" width="800" loading="eager" fetchpriority="high"
              sizes="(max-width: 640px) 100vw, (max-width: 1024px) 50vw, 800px"
            />
          </div>
        </div>

        <div class="mx-auto max-w-4xl px-4 py-12 space-y-8">
          <!-- Daily Profit Section -->
          <div class="min-h-screen bg-white dark:bg-black">
            <!-- Header Section -->
            <div class="text-center text-inherit">
              <h1 class="mb-2 text-4xl font-bold">
                {{ $t('analysis.hero1.title') }}
              </h1>
              <p class="mx-auto max-w-2xl text-lg">
                {{ $t('analysis.hero1.subtitle') }}
              </p>
            </div>

            <!-- Commission Sections -->
            <div class="mb-6 border border-gray-100 rounded-xl bg-white p-6 shadow-sm transition-all hover:border-emerald-100 hover:shadow-lg">
              <h2 class="mb-6 border-b border-emerald-100 pb-2 text-2xl text-gray-800 font-semibold">
                {{ $t('analysis.hero1.title1') }}
              </h2>
              <div class="flex flex-wrap items-center gap-4 rounded-lg bg-gray-50 px-4 py-3 font-medium">
                <div class="min-w-[120px] flex-1 basis-[calc(20%-1rem)] text-sm text-gray-700">
                  {{ $t('analysis.hero1.deposit') }}
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(20%-1rem)] text-sm text-gray-700">
                  {{ $t('analysis.hero1.turnover') }}
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(20%-1rem)] text-sm text-gray-700">
                  {{ $t('analysis.hero1.validBet') }}
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(20%-1rem)] text-sm text-gray-700">
                  {{ $t('analysis.hero1.game') }}
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(20%-1rem)] text-sm text-gray-700">
                  {{ $t('analysis.hero1.bonus') }}
                </div>
              </div>
              <div class="flex flex-wrap items-center gap-4 rounded-lg px-4 py-3 even:bg-gray-50">
                <div class="min-w-[120px] flex-1 basis-[calc(20%-1rem)] text-sm text-gray-700">
                  ₱100.00
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(20%-1rem)] text-sm text-gray-700">
                  10X
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(20%-1rem)] text-sm text-gray-700">
                  ₱1,000.00
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(20%-1rem)] text-sm text-gray-700">
                  {{ $t('analysis.hero1.fishSlot') }}
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(20%-1rem)] text-sm text-emerald-600 font-bold">
                  ₱50
                </div>
              </div>
            </div>

            <!-- Agent Level Commission -->
            <div class="mb-6 border border-gray-100 rounded-xl bg-white p-6 shadow-sm transition-all hover:border-emerald-100 hover:shadow-lg">
              <h2 class="mb-6 border-b border-emerald-100 pb-2 text-2xl text-gray-800 font-semibold">
                {{ $t('analysis.agentLevels.title') }}
              </h2>
              <div class="mb-4 flex flex-wrap gap-4 rounded-lg bg-gray-50 px-4 py-3 font-medium">
                <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-gray-700">
                  {{ $t('analysis.agentLevels.headers') }}
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-gray-700">
                  {{ $t('analysis.agentLevels.headers2') }}
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-gray-700">
                  {{ $t('analysis.agentLevels.headers3') }}
                </div>
              </div>
              <div class="space-y-2">
                <div class="flex flex-wrap items-center gap-4 rounded-lg px-4 py-3 even:bg-gray-50">
                  <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-gray-700">
                    {{ $t('analysis.agentLevels.level1') }}
                  </div>
                  <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-gray-700">
                    {{ $t('analysis.agentLevels.division2') }}
                  </div>
                  <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-emerald-600">
                    0.1%
                  </div>
                  <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-gray-700">
                    {{ $t('analysis.agentLevels.level2') }}
                  </div>
                  <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-gray-700">
                    {{ $t('analysis.agentLevels.division3') }}
                  </div>
                  <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-emerald-600">
                    0.3%
                  </div>
                  <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-gray-700">
                    {{ $t('analysis.agentLevels.level3') }}
                  </div>
                  <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-gray-700">
                    {{ $t('analysis.agentLevels.division4') }}
                  </div>
                  <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-emerald-600">
                    0.05%
                  </div>
                </div>
              </div>
            </div>
            <!-- Turnover Commissions -->
            <div class="mb-6 border border-gray-100 rounded-xl bg-white p-6 shadow-sm">
              <h2 class="mb-6 border-b border-gray-200 pb-2 text-2xl text-black font-semibold">
                {{ $t('analysis.turnover.title') }}
              </h2>

              <div class="mb-4 flex flex-wrap gap-4 rounded-lg bg-gray-50 px-4 py-3 font-medium">
                <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-black">
                  {{ $t('analysis.turnover.title1') }}
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-black">
                  {{ $t('analysis.turnover.title2') }}
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-black">
                  {{ $t('analysis.turnover.title3') }}
                </div>
              </div>

              <div class="flex flex-wrap items-center gap-4 rounded-lg px-4 py-3 even:bg-gray-50">
                <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-emerald-600">
                  1+
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-emerald-600">
                  1%
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(33.33%-1rem)] text-sm text-black space-y-1">
                  <p>{{ $t('analysis.turnover.slot') }}</p>
                  <p>{{ $t('analysis.turnover.fishing') }}</p>
                </div>
              </div>
            </div>

            <!-- Recruitment Commissions -->
            <div class="border border-gray-100 rounded-xl bg-white p-6 shadow-sm">
              <h2 class="mb-6 border-b border-gray-200 pb-2 text-2xl text-black font-semibold">
                {{ $t('analysis.recruitment.title') }}
              </h2>

              <div class="mb-4 flex flex-wrap gap-4 rounded-lg bg-gray-50 px-4 py-3 font-medium">
                <div class="min-w-[120px] flex-1 basis-[calc(50%-1rem)] text-sm text-black">
                  {{ $t('analysis.recruitment.members1') }}
                </div>
                <div class="min-w-[120px] flex-1 basis-[calc(50%-1rem)] text-sm text-black">
                  {{ $t('analysis.recruitment.members') }}
                </div>
              </div>

              <div class="space-y-2">
                <div
                  v-for="(tier, index) in [5, 10]"
                  :key="index"
                  class="flex flex-wrap items-center gap-4 rounded-lg px-4 py-3 even:bg-gray-50"
                >
                  <div class="min-w-[120px] flex-1 basis-[calc(50%-1rem)] text-sm text-black">
                    {{ $t('analysis.recruitment.tier', { count: tier }) }}
                  </div>
                  <div class="min-w-[120px] flex-1 basis-[calc(50%-1rem)] text-sm text-emerald-600">
                    {{ $t('analysis.recruitment.bonus', { amount: tier * 10 }) }}
                  </div>
                </div>
              </div>
            </div>

            <!-- Responsive Handling -->
            <div class="flex flex-wrap items-center gap-4 px-4 py-3 md:hidden">
              <div class="min-w-[120px] flex-1 basis-full text-sm text-gray-700 md:basis-[calc(50%-1rem)]">
                <!-- Mobile-specific content -->
              </div>
            </div>

            <div class="mx-auto max-w-4xl px-4 py-4 space-y-8">
              <div class="rounded-2xl from-blue-50 to-indigo-50 bg-gradient-to-br p-2 shadow-xl transition-all dark:from-gray-800 dark:to-gray-900 md:p-2 hover:shadow-2xl">
                <div class="text-center space-y-2">
                  <h1 class="from-blue-600 to-indigo-600 bg-gradient-to-r bg-clip-text text-5xl text-transparent font-extrabold dark:from-blue-400 dark:to-indigo-400">
                    {{ $t('analysis.hero2.title') }}
                  </h1>

                  <div class="mx-auto max-w-3xl text-left space-y-1">
                    <div
                      v-for="index in 3"
                      :key="index"
                      class="group flex items-start rounded-lg p-2 transition-colors space-x-2 hover:bg-white/50 dark:hover:bg-gray-800/50"
                    >
                      <p class="text-lg text-gray-700 font-medium leading-relaxed dark:text-gray-300">
                        {{ $t(`analysis.hero2.subtitle${index === 1 ? '' : index}`) }}
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
