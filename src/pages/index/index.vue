<template>
  <div @click="clickHandle"><i-notice-bar icon="systemprompt" loop>
    湖大租车APP上线了！！！
    </i-notice-bar>
    <i-grid i-class="no-border">
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/delivery.png" />
        </i-grid-icon>
        <i-grid-label>送车到家</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/store.png" />
        </i-grid-icon>
        <i-grid-label>还车预约</i-grid-label>
    </i-grid-item>
</i-grid>
    <i-grid i-class="no-border">
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/bargain.png" />
        </i-grid-icon>
        <i-grid-label>特别优惠</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/car.png" />
        </i-grid-icon>
        <i-grid-label>顺风车租取</i-grid-label>
    </i-grid-item>
</i-grid>
    <i-grid i-class="no-border">
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/gps.png" />
        </i-grid-icon>
        <i-grid-label>导航</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/serach.png" />
        </i-grid-icon>
        <i-grid-label>车型查询</i-grid-label>
    </i-grid-item>
</i-grid>
<i-panel title="车辆推荐">
      <view class="top-padding">
      <i-card title="宝马740Li · 顶级旗舰" extra="轿车" thumb="cloud://lx-092780.6c78-lx-092780/3dcf8f8de806b1fb2dfe9b7437856d53.jpg">
        <view slot="content">日租2000/天 周租1688/天 月租1200/天</view>
        <view slot="footer">2017款 740LI</view>
      </i-card>
      <view class="top-padding"></view>
      <i-card title="奥迪A6L · 商务标杆" extra="轿车" thumb="cloud://lx-092780.6c78-lx-092780/1-151109162454.jpg">
        <view slot="content">日租700/天 周租600/天 月租400/天</view>
        <view slot="footer">奥迪A6L 2015款</view>
      </i-card>
      <view class="top-padding"></view>
      <i-card title="讴歌CDX·时尚达人" extra="MPV" thumb="cloud://lx-092780.6c78-lx-092780/1-1P911192Q9.jpg">
        <view slot="content">日租600/天 周租500/天 月租400/天</view>
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
    bindViewTap () {
      const url = '../logs/main'
      if (mpvuePlatform === 'wx') {
        mpvue.switchTab({ url })
      } else {
        mpvue.navigateTo({ url })
      }
    },
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  },

  created () {
    //cloud functions
    wx.cloud.callFunction({ name: 'user' }).then(
      res => {console.log(res)}
)


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
