# renthouse_h5

> A Vue.js project

## 预览
http://dujuncheng.com.cn:83/addresspicke#/

请点击链接预览，请在手机端，或者是移动调试工具中查看

## 需求
在我们前端业务开发过程中，填写地址表单是非常常见的需求。然而在h5页面要模拟ios 原生的惯性滚动，三级联动的地址选择框很复杂，所以很多大公司，比如说京东，小米的地址选择框在ios 端和 webapp 端无法做到统一。所以我开发了这个仿ios原生的惯性滚动的组件，可以在一定程度上解决这个问题；

## 实现
1. 自适应手机屏幕，viewport 禁止用户缩放
2. 实现了惯性滚动
3. 实现了三级联动
4. 事件节流，解决了在低端智能机上的卡顿问题
5. 暴露出惯性参数，滚动速度的接口，开发者可以传入自定义的参数

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```


