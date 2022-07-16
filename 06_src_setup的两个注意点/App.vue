<template>
  <demo @ok="achiveOk" name="张三" age="3"></demo>
</template>

<script>
import demo from './components/demo.vue'
import { ref,reactive } from 'vue'
  export default {
    name:'App',
    components:{ demo },
    setup(){
      function achiveOk(value){
        console.log(`触发了ok事件,传入回调的参数为${value}`);
      }
      return {
        achiveOk
      }
    }
  }
</script>
