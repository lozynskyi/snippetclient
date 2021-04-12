<template>
  <div class="bg-white flex items-center">
    <div class="container  flex flex-wrap items-center lg:flex-nowrap">
      <nuxt-link
        :to="{ name: 'home' }"
        class="mr-10 flex-shrink-0"
      >
        <img src="~/assets/logo.png" alt="Logo" class="h-8">
      </nuxt-link>
      <div class="w-full flex">
        <ul class="h-24 flex items-center">
          <li>
            <nuxt-link
              :to="{ name: 'home' }"
              class="text-lg text-gray-700 py-8 px-4"
            >
              Browse
            </nuxt-link>
          </li>
          <li>
            <nuxt-link
              :to="{ name: 'home' }"
              class="text-lg text-gray-700 py-8 px-4"
            >
              Search
            </nuxt-link>
          </li>
        </ul>

        <ul class="h-24 flex items-center ml-auto text-right">
          <li>
            <nuxt-link
              :to="{ name: 'home' }"
              class="text-lg text-gray-700 py-8 px-4"
            >
              Dashboard
            </nuxt-link>
          </li>
          <li>
            <nuxt-link
              :to="{ name: 'home' }"
              class="text-lg text-gray-700 py-8 px-4"
            >
              Pavlo Lozynskyi
            </nuxt-link>
          </li>
          <li>
            <nuxt-link
              :to="{ name: 'home' }"
              class="text-lg text-gray-700 py-8 px-4"
            >
              Sign In
            </nuxt-link>
          </li>
          <li>
            <nuxt-link
              :to="{ name: 'home' }"
              class="text-lg text-gray-700 py-8 px-4"
            >
              Create account
            </nuxt-link>
          </li>
          <li>
            <nuxt-link
              :to="{ name: 'home' }"
              class="text-lg text-gray-700 py-8 px-4"
            >
              Sign Out
            </nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
  export default {

  }
</script>
