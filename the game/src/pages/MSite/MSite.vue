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
          
  
</style>