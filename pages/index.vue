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
  export default {
    data: () => ({
    valid:true,
      name: '',
      passWord: '',
      password:'Password',
    }),
    methods: {
      submit () {
          this.$router.push('/home')
      }
    }
  }
</script>
