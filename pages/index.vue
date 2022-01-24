<template>
  <div>
    <Tutorial />
    <div>{{ user }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: null,
    }
  },
  async fetch() {
    const token =
      'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE2NDIyMDIwMTEsInN1YiI6IjEiLCJyZWZyZXNoIjpmYWxzZX0.EOjwKUxgTnDmZGKhaWdFrVbMua2xDejXd3PxuMQwkWg'
    const config = {
      headers: { Authorization: 'Bearer ' + token },
    }

    // const response = await fetch('http://localhost:8000/test', {
    //   credentials: 'include',
    //   'Content-Type': 'application/json',
    //   Authorization: 'Bearer ' + token,
    // })
    const response = await fetch(`http://localhost:8000/users/me`, config)
    this.user = await response.json()
    console.log(response)
    console.log(this.user)
  },
  created() {
    console.log('created')
  },
}
</script>
