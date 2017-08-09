# vue-ios-address-picker

基于vue构建的h5移动端实现仿ios三级联动原生地址滚动选择框。


## 预览
![](http://image.dydata.io/TWEb1kA6eyU3NpZZQiv2Ah.gif)

## Installation
```
1. git clone https://github.com/dujuncheng/vue-ios-address-picker.git
2. cd my-project
3. npm install 
4. npm run dev 
```

## Quick Start

1.the first thing you need todo is import this component, just like below:
```
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
```

2. you would like to adjust some params of this component to make this suited for you.

```
/* 
container-height 为奇数，表示弹出框的高度，如:container-height="5" 为5rem
selectdata 为父组件注册的方法，如：
  selectdata (data) {
    console.log(data)   // data 为用户选中的地址
  }
*/ 
<address-selector :container-height="5" v-on:selectdata="selectdata"></address-selector>
```



