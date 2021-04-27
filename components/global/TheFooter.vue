<template>
  <div class="mt-24 mb-12">
    <div class="container flex flex-wrap lg:flex-nowrap justify-between">
      <ul class="flex items-center mb-6 lg:mb-0">
        <li class="mr-16">
          <nuxt-link
            class="text-gray-500 text-sm mb-2 inline-block"
            :to="{name: 'index'}"
          >
          Home
          </nuxt-link>
          <div>
            &copy; BoringBox Ltd 2021. All rights reserved.
          </div>

        </li>
      </ul>

    </div>
  </div>
</template>
