<template>
   <div class='login-page'>                
       <input v-model="user_name"/>                
       <input v-model="password"/>    
       <button @click="login">登录</button>     
    </div> 
</template>

<script>
import {loginReq} from '@/api/user'
export default {
    data() {
        return {
            user_name:'weibin',
            password:''
        }
    },
    methods:{
        login() {
            loginReq({ user_name: this.user_name, password: this.password }).then((res) => {       
                  console.log(res.data)    
            }) 
        }
    }
}
</script>

