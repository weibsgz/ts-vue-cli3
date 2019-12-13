<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import {loginReq} from '@/api/user'

export default {
  name: 'home',
  mounted() {
      loginReq({username:'weibin',password:123}).then(res=>{
         console.log(res.data.code)
     })
  },
  components: {
    HelloWorld
  }
}
</script>
