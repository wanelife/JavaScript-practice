<template>
  <section class="msite">
    <div class="huadong">
      <div class="bt">
        <nav>
          <span @click="qh(index)"
                v-for="(item,index) in list"
                :class="{active:show==index+1}"
                :key="index">
            {{item}}
          </span>
        </nav>
      </div>         
    </div>
    <div class="search">
      <i class="iconfont icon-search"></i>
    </div>
    <div>
      <van-swipe class="my-swipe" :autoplay="3000" indicator-color="white"  >
        <van-swipe-item><van-image
          alt="111"
          width="300"
          height="150"
          src="http://i-4.yxdown.com/2020/6/17/90f5db59-4679-454b-81bd-1ed203628b8a.jpg"
        /></van-swipe-item>
        <van-swipe-item><van-image
          alt="222"
          width="300"
          height="150"
          src="http://i-4.yxdown.com/2020/6/17/c5b2b731-4dc1-4dc4-8aed-af69a717a1f4.jpg"
        /></van-swipe-item>
        <van-swipe-item><van-image
          alt="333"
          width="300"
          height="150"
          src="http://i-4.yxdown.com/2020/6/17/e478ffa4-2c7d-4a5e-b4b0-919780b639a4.jpg"
        /></van-swipe-item>
        <van-swipe-item><van-image
          alt="444"
          width="300"
          height="150"
          src="http://i-4.yxdown.com/2019/9/19/KDEyMHgxMjAp/011f505c-fa69-4df8-aa75-d983d47eda79.png"
        /></van-swipe-item>
      </van-swipe>
    </div>
  
    
  </section>

</template>

<script>
  import { mapState } from 'vuex'

  export default {
    data () {
    return {
      index: 0,
      show: 1,
      list: ["关注", "头条", "热门", "游戏", "科技", "影视", "硬件"],
      
    }
  },
  methods: {
    qh: function (index) {
      this.index = index;    
      if (this.index == index) {
        this.show = index + 1;
      }
    }
  },

 }
</script>

<style lang="stylus" rel="stylesheet/stylus">
.huadong {
  width: 90%;
  
}
.bt {
  width: 100%;
  height: 50px;
  background-color: white;
  border-bottom: hidden;
  overflow: hidden;
}

nav {
  padding: 0 10px;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: middle;
  -ms-flex-align: middle;
  align-items: middle;
  overflow: auto;
}
span {
  height: 50px;
  line-height: 50px;
  display: inline-block;
  width: 45px;
  font-weight: bolder;
  text-align: center;
  margin-left: 10px;
  -ms-flex-negative: 0; 
  flex-shrink: 0;
  color: gray;
  
}
.active {
  color:black;
  font-size: 18px;
}
.search{
  position: absolute;
  right: 0;
  top: 13px;
}
.iconfont{
  font-size: 25px;
}
.my-swipe .van-swipe-item {
    text-align: center;
  }
        
  
</style>