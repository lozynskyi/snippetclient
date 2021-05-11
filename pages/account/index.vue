<template>
  <div class="container mt-16">
    <div class="flex flex-col items-center">
      <h1 class="text-3xl text-gray-700 font-medium mb-10">
        {{ $auth.user.user.name }}
      </h1>

      <div class="w-full md:w-6/12 lg:w-4/12 mb-6">
        <form
          action="#"
          class="mb-6"
          @submit.prevent="submit"
        >
          <div class="mb-6">
            <label
              for="email"
              class="block text-gray-600 font-medium mb-2"
              :class="{
              'text-red-500': validation.email
            }"
            >
              Email address
            </label>
            <input
              type="text"
              name="email"
              id="email"
              class="border-2 border-gray-400 rounded block w-full p-3"
              :class="{
              'border-red-500': validation.email
            }"
              v-model="form.email"
            >
            <div class="text-red-500 mb-4 font-medium text-sm mt-1" v-if="validation.email">
              {{ validation.email[0] }}
            </div>
          </div>

          <div class="mb-6">
            <label
              for="password"
              class="block text-gray-600 font-medium mb-2"
              :class="{
              'text-red-500': validation.password
            }"
            >
              Password
            </label>
            <input
              type="password"
              name="password"
              id="password"
              class="border-2 border-gray-400 rounded block w-full p-3"
              :class="{
              'border-red-500': validation.password
            }"
              v-model="form.password"
            >
            <div class="text-red-500 mb-4 font-medium text-sm mt-1" v-if="validation.password">
              {{ validation.password[0] }}
            </div>
          </div>

          <div>
            <button type="submit" class="bg-blue-500 text-white p-4 rounded text-center font-medium">
              Update
            </button>
          </div>

        </form>
        <div>
          <nuxt-link
            :to="{
            name: 'author-id',
            params: {
              id: $auth.user.user.username
            }
          }"
          >
            View your public profile
          </nuxt-link>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
  export default {
    middleware: [
      'auth'
    ],
    data() {
      return {
        form: {
          email: '',
          password: '',
          name: '',
          username: ''
        },
        validation: {}
      }
    },
    head () {
      return {
        title: 'Account'
      }
    },
    methods: {
      async submit() {
        try {

        } catch (e) {
          console.log(e)
          if (e.response.status === 422) {
            this.validation = e.response.data.errors
          }
          if (e.response.status === 401) {
            this.validation = e.response.data.errors
          }
        }
      }
    }
  }
</script>
