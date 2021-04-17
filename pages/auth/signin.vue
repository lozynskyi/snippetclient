<template>
  <div class="container mt-16">
    <div class="flex flex-col items-center">
      <h1 class="text-3xl text-gray-700 font-medium mb-10"> Hello </h1>
    </div>
    <a href="" @click.prevent="submit">sign in</a>
  </div>
</template>

<script>
  export default {
    methods: {
      async submit() {
        await this.$auth.loginWith('local', {
          data: {
            email: 'valera.popkin@gmx.com',
            password: 'password'
          }
        })

      }
    }
  }
</script>
