<template>
  <div @keydown.enter="handleSubmit">
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
  &nbsp;  <button @click="handleSubmit">Submit</button> //bad form
  </div>
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
