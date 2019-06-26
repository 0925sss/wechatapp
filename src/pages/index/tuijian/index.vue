<template>
  <div @click="clickHandle">
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
      motto: 'Hello miniprograme',
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
      }
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
div >>> .no-border {
  border-width: 0pt;
}
.top-padding {
  padding-top: 50rpx;
}
.userinfo {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.userinfo-avatar {
  width: 128rpx;
  height: 128rpx;
  margin: 20rpx;
  border-radius: 50%;
}

.userinfo-nickname {
  color: #aaa;
}

.usermotto {
  margin-top: 150px;
}

.form-control {
  display: block;
  padding: 0 12px;
  margin-bottom: 5px;
  border: 1px solid #ccc;
}
.all{
  width:7.5rem;
  height:1rem;
  background-color:blue;
}
.all:after{
  display:block;
  content:'';
  clear:both;
}
.left{
  float:left;
  width:3rem;
  height:1rem;
  background-color:red;
}

.right{
  float:left;
  width:4.5rem;
  height:1rem;
  background-color:green;
}
</style>
