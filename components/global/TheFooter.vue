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
          <div class="text-gray-500 text-sm">
            &copy; BoringBox Ltd 2021. All rights reserved.
          </div>
        </li>
      </ul>

      <ul class="flex items-center">
        <li class="mr-8">
          <a
            class="text-gray-500 text-sm"
            href="https://github.com"
            target="_blank"
            rel="noopener"
          >
            github.com
          </a>
        </li>
      </ul>

    </div>
  </div>
</template>
