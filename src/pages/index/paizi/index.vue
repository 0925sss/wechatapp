<template>
  <div @click="clickHandle">
<i-panel title="汽车租赁公司简介">
      <view class="top-padding">
      <i-card title="神州汽车租赁有限公司" thumb="cloud://lx-092780.6c78-lx-092780/shen (3).jpg">
        <view slot="content">神州租车 (China Auto Rental)成立于2007年9月，总部位于中国北京。作为中国汽车租赁行业的领跑者，神州租车积极借鉴国际成熟市场成功的汽车租赁模式，并结合中国客户的消费习惯，为广大消费者提供短租、长租及融资租赁等专业化的汽车租赁服务，以及GPS 导航、道路救援等完善的配套服务。</view>
      </i-card>
      <view class="top-padding"></view>
      <i-card title="大方租车" thumb="cloud://lx-092780.6c78-lx-092780/da.jpg">
        <view slot="content">大方租车总部设于武汉，现营运车辆逾千台，服务的个人客户数万名，企业客户数百家，以稳健、高速发展之势居于行业领先前列。大方租车始终秉持“全民租车倡导者”的使命，力求让租车这种更经济、更环保的出行方式为更多大众接受和受益。借鉴国内外领先的连锁租车模式，创建了电子商务化管理平台和客服24小时呼叫中心，凭借时尚多样的车型选择、真诚贴心的服务意识，以及便捷自由的租车模式，为客户提供了全新的租车服务体验。</view>
      </i-card>
      <view class="top-padding"></view>
      <i-card title="一嗨租车网" thumb="cloud://lx-092780.6c78-lx-092780/yi.jpg">
        <view slot="content">上海一嗨汽车租赁有限公司（简称“一嗨租车”）是中国最大的连锁租车服务提供商。公司总部设立于上海，分公司遍布全国一、二线及各大省会城市，拥有各种车型几千辆，服务范围遍布70多个城市，是一家覆盖全国、以高质量服务满足客户需求的大型现代交通服务企业。一嗨租车始终坚持以“分享、环保、节能、减排、和谐”为企业理念，通过为消费者开发“时尚、自由、创新”的产品，力求让租车这种绿色分享的出行方式为更多人所接受。</view>
      </i-card>
      <view class="top-padding"></view>
    </view>
    </i-panel>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
    }
  },

  components: {
    card
  },

  methods: {
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
</style>
