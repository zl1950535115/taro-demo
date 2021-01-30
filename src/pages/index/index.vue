<template>
  <view class="index">
    <text>{{ msg }}{{ store }}</text>
  </view>
</template>

<script>
import './index.scss';
import Taro from '@tarojs/taro';

export default {
  data () {
    return {
      msg: 'Hello world!',
      store:'222'
    }
  },
  created() {
    console.log('111')
  },
  mounted(){
    Taro.setStorageSync('key','数据')
    Taro.setStorageSync('foodKey', 'vue');
    this.store = Taro.getStorageSync('foodKey')
  }
}
</script>
