<template>
  <div>
    <h2>Login</h2>
    <form @submit.prevent="userLogin">
      <span class="p-float-label">
        <InputText id="username" v-model="login.username" type="text" />
        <label for="username">Username</label>
      </span>
      <span class="p-float-label">
        <InputText id="password" v-model="login.password" type="password" />
        <label for="password">password</label>
      </span>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
import InputText from 'primevue/inputtext'

export default {
  components: {
    InputText,
  },
  data() {
    return {
      login: {
        username: '',
        password: '',
      },
    }
  },
  methods: {
    // async userLogin() {
    //   try {
    //     const fdata = new FormData()
    //     fdata.append('username', this.login.username)
    //     fdata.append('password', this.login.password)
    //     const response = await this.$axios.post(
    //       'http://localhost:8000/auth/login',
    //       // fdata,
    //       this.login,
    //       {
    //         headers: {
    //           'X-Requested-With': 'XMLHttpRequest2',
    //           // 'Content-Type': 'application/x-www-form-urlencoded',
    //         },
    //       }
    //     )
    //     console.log(response)
    //   } catch (err) {
    //     console.log(err)
    //   }
    // },
    // NUXTAUTH
    async userLogin() {
      try {
        const fdata = new FormData()
        console.log(fdata.values())
        fdata.append('username', this.login.username)
        fdata.append('password', this.login.password)
        console.log(fdata.values())
        const response = await this.$auth.loginWith('local', {
          data: this.login,
        })
        console.log(response)
      } catch (err) {
        console.log(err)
      }
    },
  },
}
</script>

<style></style>
