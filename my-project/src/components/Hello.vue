<template>
  <div class="container">
    <input type="text" placeholder="请输入您的姓名" class="item" >
    <input type="text" placeholder="请输入您的年龄" class="item" >
    <input type="number" placeholder="请输入您的手机号" class="item" >
    <addresspicker :container-height="7" v-on:selectdata="selectdata" class="item" :inertia="inertia" :speed="speed"></addresspicker>
    <div class="controller-container">
      <div class="title">
        <p>您可以在这里调整组件的参数</p>
      </div>
      <div class="speed-container">
        <div class="speed-title">滚动速度</div>
        <el-slider v-model="speed" show-input class="speed-control"></el-slider>
      </div>
      <div class="inertia-container">
        <div class="inertia-title">阻力大小</div>
        <el-slider v-model="inertia" show-input class="inertia-control"></el-slider>
      </div>
      <div class="desc">
        <p>貌似饿了么的ui不支持移动端的滑动？那就点击右侧的加减</p>
      </div>
    </div>
  </div>
</template>

<script>
import addresspicker from '@/components/addressSelector';
export default {
  name: 'hello',
  data () {
    return {
      title: '请输入您的个人信息',
      inertia:30,
      speed:12
    }
  },
  components:{
    addresspicker
  },
  methods:{
    selectdata (data) {
      console.log(data)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .inertia-container{
    height: 1rem;
    display: flex;
  }
  .inertia-title{
    flex: 1;
    font-size: 0.35rem;
  }
  .inertia-control{
    flex: 4;
  }

  .speed-container{
    height: 1rem;
    display: flex;
  }
  .speed-title{
    flex: 1;
    font-size: 0.35rem;
  }
  .speed-control{
    flex: 4;
  }
  .controller-container{
    padding: 80px 20px;
  }
  .container{
    font-size: 0.5rem;
  }
 .item{
   -web-kit-appearance:none;
   -moz-appearance: none;
   border: none;
   outline:medium;
   width: 100%;
   height: 1rem;
   border-bottom: 1px solid gainsboro;
   box-sizing: border-box;
   line-height: 1rem;
   font-size: 0.35rem;
   text-align: left;
   padding-left: 0.5rem;
 }
</style>
