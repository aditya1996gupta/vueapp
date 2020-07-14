<template>
<div>
<br />
<h1>Simple Modal Notifications in Vue.js with Vue-SweetAlert2</h1>
  <button v-on:click="alertDisplay">Name</button> &nbsp;
  <button v-on:click="ad">Heading</button> &nbsp;
  <button v-on:click="ad2">Delete</button> &nbsp;
  <button v-on:click="ad3">emaphazied</button> &nbsp;
</div>
</template>

<script>
export default {
  data () {
    return {
      text: ''
    }
  },
  methods: {
    ad3 () {
      this.$swal({
        title: 'Custom HTML',
        // add a custom html tags by defining a html method.
        html:
            'This is an <em> emaphazied text </em>, ' +
            '<a href="">links</a> ' +
            '<strong>And other tags</strong>',
        showCloseButton: true,
        showCancelButton: true,
        focusConfirm: false
      })
    },
    ad2 () {
      this.$swal({
        title: 'Are you sure?',
        text: 'You can\'t revert your action',
        type: 'warning',
        showCancelButton: true,
        confirmButtonText: 'Yes Delete it!',
        cancelButtonText: 'No, Keep it!',
        showCloseButton: true,
        showLoaderOnConfirm: true
      }).then((result) => {
        if (result.value) {
          this.$swal('Deleted', 'You successfully deleted this file', 'success')
        } else {
          this.$swal('Cancelled', 'Your file is still intact', 'info')
        }
      })
    },
    ad () {
      this.$swal('Heading', 'this is a Heading', 'OK')
    },
    alertDisplay () {
      // Adding an input method from SweetAlert 2 automatically binds an input form.
      this.$swal({
        title: 'What is your Name?',
        input: 'text',
        inputPlaceholder: 'Enter your name here',
        showCloseButton: true
      })
    }
  }
}
</script>
