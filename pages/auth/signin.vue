<template>
  <div class="container mt-16">
    <div class="flex flex-col items-center">
      <h1 class="text-3xl text-gray-700 font-medium mb-10"> Hello. </h1>

      <form action="#" class="bg-white p-8 rounded w-full md:w-6/12 lg:w-4/12 mb-6" onclick.prevent="">
        <div class="mb-6">
          <label for="email" class="block text-gray-600 font-medium mb-2">Email address</label>
          <input
            type="text"
            name="email"
            id="email"
            class="border-2 border-gray-400 rounded block w-full p-3"
          >
        </div>

        <div class="mb-6">
          <label for="password" class="block text-gray-600 font-medium mb-2">Password</label>
          <input
            type="password"
            name="password"
            id="password"
            class="border-2 border-gray-400 rounded block w-full p-3"
          >
        </div>
      </form>

    </div>

    <a href="" @click.prevent="submit">sign in</a>
  </div>
</template>

<script>
  import Index from "@/pages";
  export default {
    components: {Index},
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
