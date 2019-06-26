<template>
  <div @click="clickHandle">
  <view class="userinfo">
    <view class="userinfo-avatar">
    <open-data type="userAvatarUrl"></open-data>
    </view>
    <open-data type="userNickName"></open-data>
  </view>

  <i-button type="ghost" @click="handleClick"  size="large">点个赞支持一下吧！</i-button>
  <i-toast id="toast" />
  </div>
</template>

<script>
const { $Toast } = require('../../../static/dist/base/index');
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
    handleClick  (){
        $Toast({
            content: '万分感谢',
            type: 'success'
        });
    },
  },
  

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
.userinfo {
position: relative;
width: 750rpx;
height: 320rpx;
color: #666;
display: flex;
flex-direction: column;
align-items: center;
}
 
.userinfo-avatar {
overflow:hidden;
display: block;
width: 160rpx;
height: 160rpx;
margin: 20rpx;
margin-top: 50rpx;
border-radius: 50%;
border: 2px solid #fff;
box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.2);
}
</style>
