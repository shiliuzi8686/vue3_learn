<template>
  <h1>个人信息</h1>
  <h2>姓名:{{name}}</h2>
  <h2>年龄:{{age}}</h2>
  <button @click="emitOk">触发ok事件</button>
</template>

<script>
import { ref,reactive } from 'vue'
  export default {
    name:'App',
    props:['name','age'],
    emits:['ok'],
    setup(props,content){
      console.log(content)
      function emitOk(){
        content.emit('ok','子组件传参')
      }
      // 返回一个对象（）常用
      return {
        emitOk
      }
    }
  }
</script>
