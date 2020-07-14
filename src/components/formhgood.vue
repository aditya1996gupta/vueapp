<template>
  <!-- @submit handles any form of submission. -->
  <!-- .prevent keeps the event from bubbling around and doing anything else. -->
  <form @submit.prevent="handleSubmit">
    <label>
      Email:
      <input type="email" v-model="user.email"/>
    </label>
    <label>
      Name:
      <input type="text" v-model="user.name"/>
    </label>
    <label>
      Password:
      <input type="password" v-model="user.password"/>
    </label>
  &nbsp;  <button type="submit">Submit</button> //good form
  </form>
</template>

<script>
export default {
  data () {
    return {
      user: {
        email: '',
        name: '',
        password: ''
      }
    }
  },

  methods: {
    handleSubmit () {
      // Send data to the server or update your stores and such.
    }
  }
}
</script>
