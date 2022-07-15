<template>
  <h1>个人信息</h1>
  <h2>姓名</h2>
  <h2>年龄</h2>
  <button @click="sayHello">说话</button>
</template>

<script>
import { h } from "vue";
  export default {
    name:'App',
    setup(){
      // 数据
      let name = '张三'
      let age = 18
      // 方法
      function sayHello(){
        alert(`我叫${name},我${age}岁了`)
      }
      // 返回一个对象（）常用
      return {
        name,
        age,
        sayHello
      }

      // 返回一个渲染函数
      // h函数：参数一：放入页面的元素，参数二：该元素的内容
      // h函数：返回的是一个创建好的元素+内容（自称模板）
      // return () => h('h1','ok')
    }
  }
</script>
