<template>
  <h1>个人信息</h1>
  <h2>姓名:{{name}}</h2>
  <h2>年龄:{{age}}</h2>
  <!-- 模板里不需要 .value 会自动读取响应式对象中的value -->
  <h2>另一个人的信息：{{user.name}}-{{user.age}}</h2>
  <button @click="infoChange">修改人的信息</button>
  <button @click="otherInfoChange">修改另一个人的信息</button>
</template>

<script>
import { ref } from 'vue'
  export default {
    name:'App',
    setup(){
      // 数据
      let name = ref('张三') // ref返回的是一个响应式对象
      let age = ref(18)
      let user = ref({
        name:'湖理',
        age:1
      })
      // 方法
      function infoChange(){
        // 修改响应式对象的值
        name.value = '李四'
        age.value = 28
      }
      function otherInfoChange(){
        // 修改响应式对象的值
        user.value.name = '理工'
        user.value.age = 3
        // console.log(user.value)
      }
      // 返回一个对象（）常用
      return {
        name,
        age,
        user,
        infoChange,
        otherInfoChange
      }
    }
  }
</script>
