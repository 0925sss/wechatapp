<template>
  <div @click="clickHandle">
<i-panel title="汽车小知识">
      <view class="top-padding">
      <i-card title="汽车后备箱">
        <view slot="content">我们必须要了解的知识就是汽车内部也有逃生舱，那就是后备箱了，其实后备箱的作用也是非常大的，并不是只是单纯的用来存放东西而已，如果一不小心我们的车辆发生了危险事故，在车门和车窗都不能打开的情况下就可以利用后备箱来逃生，这个时候车子里面的人员可以爬到车子后面的后备箱，找到后备箱的逃生拉环就可以成功自救了。</view>
      </i-card>
      <view class="top-padding"></view>
      <i-card title="安全气囊">
        <view slot="content">汽车上的安全气囊是不能够一直使用的，一般来说安全气囊的使用寿命和汽车是相同的，但是实际上并不是这样的，其实我们也不知道安全气囊具体能够用多长时间，万一安全气囊坏了的话，发生意外的时候，那可就非常危险了。一般来说，如果我们发现指示灯一直在闪烁，或者说汽车有一些其他一样的话，那么这个时候我们就需要注意了，很有可能是安全气囊出现了一些问题就需要及时的到维修店去进行相关的检测，看看有没有出现问题，如果有问题的话及时更换维修就可以了。</view>
      </i-card>
      <view class="top-padding"></view>
      <i-card title="座椅位置调节">
        <view slot="content">我们在开车的时候尽量的离方向盘远一点，在日常生活当中，我们经常能够看到一些身材矮小的人，在开车的时候把自己的座位调得很靠前，因为对于他们来说这样的坐姿也能够让他们更轻松的打方向，但其实这样的做法还是有很大安全隐患的，如果一旦发生了紧急情况，安全气囊就不能发挥出它最好的作用。</view>
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
