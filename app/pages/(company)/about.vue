<script setup lang="ts">
const { t } = useI18n({
  useScope: 'local',
})

const paragraphs: { [key: number]: string } = {
  1: t('about.paragraphs.introduction'),
  2: t('about.paragraphs.mission'),
  3: t('about.paragraphs.goal'),
  4: t('about.paragraphs.importance'),
  5: t('about.paragraphs.closing'),
}
const seoImage = 'https://images.pexels.com/photos/27050060/pexels-photo-27050060.jpeg'
useLangMeta('about.meta', seoImage, 'prefix', t)
</script>

<template>
  <InternalPage :title="t('about.title')">
    <template #content>
      <p v-for="(paragraph, index) in paragraphs" :key="index" class="leading-relaxed">
        {{ paragraph }}
      </p>
    </template>
  </InternalPage>
</template>

<i18n lang="json">
{
    "en": {
        "about": {
            "title": "About Me777.com",
            "paragraphs": {
                "introduction": "ME777 is one of the world's most renowned online gambling operators including live casino.",
                "mission": "Offering a thrilling and entertaining range of games",
                "goal": "Chess, slot games, fishing, lottery, and sports betting.",
                "importance": "It is authorized and regulated by the government of Curaçao and operates under license number Antillephone issued to 8048/JAZ.",
                "closing": " It has passed all compliance checks and holds legal authorization to conduct all gaming operations involving opportunities and betting."
            },
            "meta": {
                "description": "Xanzhu.com - Your cybersecurity hub. Protecting you online with valuable insights on security, privacy, and accessibility. Join us!",
                "title": "About"
            }
        }
    },
    "ko": {
        "about": {
            "title": "tungkol sa Me777.com",
            "paragraphs": {
             "introduction": "Ang ME777 ay isa sa pinakatanyag na operator ng online na sugal sa buong mundo, kasama ang live na casino.",
             "mission": "Nag-aalok ng nakakasabik at nakakaaliw na hanay ng mga laro",
             "goal": "Chess, mga slot game, pangingisda, loterya, at pagtaya sa sports",
              "importance": "Awtorisado at regulado ito ng pamahalaan ng Curaçao at nagpapatakbo sa ilalim ng lisensyang Antillephone na may bilang na 8048/JAZ.",
             "closing": "Nakapasa sa lahat ng pagsusuri sa pagsunod at may legal na awtorisasyon para sa lahat ng operasyong may kinalaman sa pagkakataon at pagtaya."
            },
            "meta": {
                "description": "Xanzhu.com - 사이버 보안 허브. 보안, 프라이버시, 접근성에 대한 유용한 통찰로 온라인에서 여러분을 보호합니다. 함께하세요!",
                "title": "소개"
            }
        }
    },
    "zh": {
        "about": {
            "title": "关于 Me777.com",
            "paragraphs": {
                "introduction": "ME777 是全球最著名的在线博彩运营商之一，提供真人娱乐场等游戏。",
                "mission": "提供一系列刺激且娱乐性强的游戏 ",
                "goal": "国际象棋、老虎机、捕鱼游戏、彩票和体育博彩  ",
                "importance": "获得库拉索政府授权和监管，并持有 Antillephone 颁发的许可证（编号：8048/JAZ）。",
                "closing": "已通过所有合规检查，并拥有开展涉及机会与投注的所有游戏业务的合法授权。"
            },
            "meta": {
                "description": "Xanzhu.com - 您的网络安全中心。通过关于安全、隐私和可访问性的宝贵见解，守护您的网络安全。加入我们！",
                "title": "关于"
            }
        }
    }
}
</i18n>
