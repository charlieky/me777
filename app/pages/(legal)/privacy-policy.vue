<script setup lang="ts">
const { t } = useI18n({
  useScope: 'local',
})

const paragraphs: { [key: number]: string } = {
  1: t('PP.section-one'),
  2: t('PP.section-two'),
  3: t('PP.section-three'),
  4: t('PP.section-four'),
  5: t('PP.section-five'),
  6: t('PP.section-six'),
  7: t('PP.section-seven'),
  8: t('PP.section-eight'),
}

// SEO Metadata
const seoImage = 'https://images.pexels.com/photos/27286458/pexels-photo-27286458.jpeg'
useLangMeta('PP', seoImage, 'prefix', t)
</script>

<template>
  <InternalPage :title="t('PP.title')" :description="t('PP.description')" :datelabel="t('PP.date')">
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
    "PP": {
      "title": "Privacy Policy",
      "description": "Read our privacy policy statement",
      "date": "Last Updated",
      "section-one": "1. Affiliate  commissions  range  from  30%  to  50%, depending on the  number  of your  monthly  active  players  and their  net losses.",
      "section-two": "2. NGR Commissions  are  calculated on a monthly basis.",
      "section-three": "3. To qualify for commission calculation, you need a minimum of  2 deposited  and active  players  each  month.",
      "section-four": "4. An active player  is defined  as  someone  who makes  a deposit  and  plays, with  a minimum deposit  &  turnover  of  100  required to be counted  as active.",
      "section-five": "5. A 16% to between  22%  deduction  from  the  player’s profit and loss is allocated for operation costs.",
      "section-six": "6. Deductions  may be made  from your  revenue share  if your  players  re involved in collusion or  fraudulent  activities, at the discretion  of  the  me777",
      "section-seven": "7. Commissions can be withdrawn no later  than noon on the  third day  after  system settlement.",
      "section-eight": "8. Negative  balances  will not carried  over  to  the  next  settlement  period."
    }
  },
  "ko": {
    "PP": {
      "title": "Patakaran sa Privacy",
      "description": "Basahin ang aming pahayag sa patakaran sa privacy",
     "date": "Huling Na-update",
      "section-one": "1. Ang komisyon ng Affiliate ay mula 30% hanggang 50%, depende sa bilang ng iyong mga aktibong manlalaro buwan-buwan at kanilang netong pagkalugi.",
      "section-two": "2. Ang mga Komisyon batay sa NGR ay kinakalkula buwan-buwan.",
      "section-three": "3. Upang maging karapat-dapat sa pagkalkula ng komisyon, kailangan ng hindi bababa sa 2 deposito at aktibong manlalaro bawat buwan.",
      "section-four": "4. Ang aktibong manlalaro ay tinukoy bilang isang nagdeposito at naglaro, na may minimum na deposito at turnover na 100 upang mabilang bilang aktibo.",
      "section-five": "5. Ang 16% hanggang 22% na bawas mula sa kita at lugi ng manlalaro ay inilalaan para sa mga gastos sa operasyon.",
      "section-six": "6. Maaaring bawasin sa iyong bahagi ng kita kung ang iyong mga manlalaro ay sangkot sa pagkakuntsaba o mapanlinlang na mga gawain, ayon sa pagpapasya ng me777.",
      "section-seven": "7. Maaaring i-withdraw ang mga komisyon hindi lalampas sa tanghali ng ikatlong araw pagkatapos ng settlement ng system.",
      "section-eight": "8. Ang mga negatibong balanse ay hindi dadalhin sa susunod na panahon ng settlement."
    }
  },
  "zh": {
    "PP": {
      "title": "隐私政策",
      "description": "查看我们的隐私政策声明",
      "date": "最后更新",
      "section-one": "1. 联盟佣金范围为30%至50%，具体取决于您每月活跃玩家数量及其净损失。",
      "section-two": "2. 净博彩收入(NGR)佣金按月计算。",
      "section-three": "3. 要获得佣金计算资格，每月需至少有2名存款并活跃的玩家。",
      "section-four": "4. 活跃玩家定义为进行存款并游戏的用户，最低存款与流水需达到100方可计为活跃。",
      "section-five": "5. 玩家盈亏的16%至22%将作为运营成本扣除。",
      "section-six": "6. 若您的玩家涉及共谋或欺诈行为，me777有权酌情从您的收入分成中扣除相应金额。",
      "section-seven": "7. 佣金需在系统结算后第三天中午前完成提现。",
      "section-eight": "8. 负余额不会结转至下一结算周期。"
    }
  }
}
</i18n>
