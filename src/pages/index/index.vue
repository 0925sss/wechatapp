<template>
  <div @click="clickHandle"><i-notice-bar icon="systemprompt" loop>
    湖大租车APP上线了！！！
    </i-notice-bar>
    <i-grid i-class="no-border">
    <i-grid-item @click="tozhishi">
        <i-grid-icon>
            <image src="/static/grid/delivery.png" />
        </i-grid-icon>
        <i-grid-label>汽车知识</i-grid-label>
    </i-grid-item>
    <i-grid-item @click="totuijian">
        <i-grid-icon>
            <image src="/static/grid/store.png" />
        </i-grid-icon>
        <i-grid-label>车型推荐</i-grid-label>
    </i-grid-item>
</i-grid>
    <i-grid i-class="no-border">
    <i-grid-item @click="topaizi">
        <i-grid-icon>
            <image src="/static/grid/bargain.png" />
        </i-grid-icon>
        <i-grid-label>租车品牌</i-grid-label>
    </i-grid-item>
    <i-grid-item @click="toSerach">
        <i-grid-icon>
            <image src="/static/grid/gps.png" />
        </i-grid-icon>
        <i-grid-label>导航</i-grid-label>
    </i-grid-item>
</i-grid>
<i-panel title="车辆推荐">
      <view class="top-padding">
      <i-card title="宝马740Li · 顶级旗舰" extra="轿车" thumb="cloud://lx-092780.6c78-lx-092780/3dcf8f8de806b1fb2dfe9b7437856d53.jpg">
        <view slot="content">发动机：3.0T L6 最大马力：326PS/5500-6500rpm 变 速 箱：8挡手自一体</view>
        <view slot="footer">2017款 740LI</view>
      </i-card>
      <view class="top-padding"></view>
      <i-card title="奥迪A6L · 商务标杆" extra="轿车" thumb="cloud://lx-092780.6c78-lx-092780/1-151109162454.jpg">
        <view slot="content">排 量：2.0T 2.5L 2.8L  类 型：三厢车  变速箱：无级变速 双离合 </view>
        <view slot="footer">奥迪A6L 2015款</view>
      </i-card>
      <view class="top-padding"></view>
      <i-card title="讴歌CDX·时尚达人" extra="MPV" thumb="cloud://lx-092780.6c78-lx-092780/1-1P911192Q9.jpg">
        <view slot="content">排量：2.0L 变速箱：自动 油耗：5L</view>
        <view slot="footer">讴歌CDX·时尚达人 2017款</view>
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
    toSerach () {
      wx.navigateTo({
        url: 'serach/main'
      })
    },
    topaizi () {
      wx.navigateTo({
        url: 'paizi/main'
      })
    },
    totuijian () {
      wx.navigateTo({
        url: 'tuijian/main'
      })
    },
    tozhishi () {
      wx.navigateTo({
        url: 'zhishi/main'
      })
    }
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
</style>
