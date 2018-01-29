<template>
<v-app>
  <v-form v-model="valid" ref="form" lazy-validation>
    <v-text-field
      label="账号"
      v-model="name"
      required
    ></v-text-field>
    <v-text-field
      label="密码"
      v-model="passWord"
      :type="password"
      required
    ></v-text-field>
    <v-btn
      @click="submit"
    >
    登录
    </v-btn>
  </v-form>
  </v-app>
</template>

<script>
import axios from 'axios'
import md5 from 'js-md5'
  export default {
    data: () => ({
    valid:true,
      name: '15151965292',
      passWord: '123456',
      password:'Password',
    }),
    methods: {
      submit () {
        let dict = {
            'Account':this.name,
            'Password':md5(this.passWord)
        }

         axios.post('https://api.ilabpower.com/uc/api/Account/Login',dict).then(data=>{
             debugger
         })
      
        this.$router.push('/home')
      }
    }
  }
</script>
