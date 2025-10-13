<script setup lang="ts">
const { t } = useI18n({
  useScope: 'local',
})

const sections = [
  {
    title: t('terms.intellectualProperty.title'),
  },
  {
    title: t('terms.userResponsibilities.title'),

  },
  {
    title: t('terms.disclaimer.title'),

  },
  {
    title: t('terms.thirdPartyLinks.title'),

  },

]

// SEO Metadata
const seoImage = 'https://images.pexels.com/photos/273209/pexels-photo-273209.jpeg'
useLangMeta('terms', seoImage, 'prefix', t)
</script>

<template>
  <InternalPage
    :title="t('terms.title')" :description="t('terms.description')"
    :datelabel="t('terms.date')"
  >
    <template #content>
      <div>
        <div v-for="(section, index) in sections" :key="index" class="mb-8">
          <h2 class="mb-4 mt-8 text-2xl text-dark-900 font-semibold dark:text-gray-100">
            {{ section.title }}
          </h2>
        </div>
      </div>
    </template>
  </InternalPage>
</template>

<i18n lang="json">
{
  "en": {
    "terms": {
      "title": "Terms of Service",
      "description": "By using you agree to our Terms of Service. Please read them carefully.",
      "date": "Last Updated",

      "intellectualProperty": {
        "title": "1. Affiliate  shall  not  register  dual/multi-agent  accounts  without  the  permission  of ME777 ,and  earn  commissions  from  the related  accounts."
      },
      "userResponsibilities": {
        "title": "2. In  order  to  protect  the  privacy  and  rights  of  all  me777  member  accounts , me777  will  not  provide  any  member  password  or  member  personal  information. Agent  at  all  levels  may  not  obtain  member  information  in  any way , or log in to down line  member  accounts  arbitrarily. If  it  is found  that the  agent  violates  the privacy  of  me777  members,  me777  reserves  the  right  to cancel  the  agent  bonus and  cancel  the  agent  account."

      },
      "disclaimer": {
        "title": "3. The  number  of  player  accounts  created by  an  agent  shall  not  duplicate  and exceed  one  for  every  single member.  me777  reserves  the right  to require members  to provide valid identification  to verify  membership, and  has the right to judge whether  there  are  duplicate  members  through  IP. In case of  violation  of  the above  provisions,  me777  has the right  to terminate  the player's game  and seal  the account  and  all commissions  earned  in the game."

      },
      "thirdPartyLinks": {
        "title": "4. If  a member  of  the  agent  is  prohibited  from enjoying  me777   games  due to violations  or  me777  refunds  the  deposit  to the  member,  me777  will  not a llocate the  corresponding  commission  to the  agent. If  the  e-wallet  and  bank  information used  by  the  agent  members  need  to be  reviewed,  me777  will with hold the relevant  commission  until  the  review  is completed."
      }

    }
  },
  "ko": {
    "terms": {
    "title": "Mga Tuntunin ng Serbisyo",
    "description": "Sa paggamit nito, sumasang-ayon ka sa aming Mga Tuntunin ng Serbisyo. Basahing mabuti ang mga ito.",
    "date": "Huling Na-update",

    "intellectualProperty": {
    "title": "1. Ang Kaakibat ay HINDI dapat magrehistro ng doble/maraming ahenteng account nang walang pahintulot ng ME777, o kumita ng komisyon mula sa mga kaugnay na account."
    },
    "userResponsibilities": {
    "title": "2. Upang protektahan ang privacy at karapatan ng lahat ng miyembro ng me777, HINDI magbibigay ang me777 ng anumang password ng miyembro o personal na impormasyon. Ang mga ahente sa lahat ng antas ay HINDI maaaring kumuha ng impormasyon ng miyembro sa anumang paraan, o basta mag-log in sa mga account ng miyembro. Kung matukoy na nilabag ng ahente ang privacy ng mga miyembro, may karapatan ang me777 na kanselahin ang bonus at account ng ahente."
    },
    "disclaimer": {
    "title": "3. Ang bilang ng player account na ginawa ng ahente ay DAPAT hindi lumampas sa isa bawat miyembro. May karapatan ang me777 na humiling ng valid na ID para patunayan ang membership, at hatulan kung may duplicate na miyembro sa pamamagitan ng IP. Sa kaso ng paglabag, may karapatan ang me777 na wakasan ang laro at isara ang account kasama ang lahat ng komisyong nakuha."
    },
    "thirdPartyLinks": {
    "title": "4. Kung ang miyembro ng ahente ay pinagbawalan sa mga laro ng me777 dahil sa paglabag o ibinalik ang deposito, HINDI ito maglalaan ng komisyon sa ahente. Kung kailangang suriin ang e-wallet at impormasyon sa bangko ng miyembro, ipagkakait ng me777 ang nauugnay na komisyon hanggang sa makumpleto ang pagsusuri."
    }
    }
  },
  "zh": {
    "terms": {
     "title": "服务条款",
    "description": "使用即表示您同意我们的服务条款，请仔细阅读。",
    "date": "最后更新",

    "intellectualProperty": {
      "title": "1. 未经ME777许可，联盟会员不得注册双重/多重代理账户，也不得从相关账户获取佣金。"
    },
    "userResponsibilities": {
      "title": "2. 为保护所有me777会员隐私及权益，me777不会提供任何会员密码或个人资料。各级代理不得以任何方式获取会员信息或擅自登录下级会员账户。若发现代理侵犯会员隐私，me777有权取消代理奖金并注销代理账户。"
    },
    "disclaimer": {
      "title": "3. 代理创建的玩家账户不得重复且每位会员仅限一个。me777有权要求会员提供有效身份证件验证身份，并通过IP判断重复会员。若违反上述规定，me777有权终止游戏并封停账户及所有游戏收益。"
    },
    "thirdPartyLinks": {
      "title": "4. 若代理会员因违规被禁止参与me777游戏或me777向会员退还存款，将不向代理发放相应佣金。如需审核代理会员使用的电子钱包及银行信息，me777将暂扣相关佣金直至审核完成。"
    }
        }
  }
}
</i18n>
