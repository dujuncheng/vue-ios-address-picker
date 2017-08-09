<template>
  <div class="container">
    <input type="text" placeholder="请输入您的姓名" class="item" >
    <input type="text" placeholder="请输入您的年龄" class="item" >
    <input type="number" placeholder="请输入您的手机号" class="item" >
    <addresspicker :container-height="5" v-on:selectdata="selectdata"></addresspicker>
  </div>
</template>

<script>
import addresspicker from '@/components/addressSelector';
export default {
  name: 'hello',
  data () {
    return {
      title: '请输入您的个人信息'
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
