<template>
  <div class="container mt-16">
    <h1 class="font-medium text-4xl">Dashboard page</h1>
    <p>A little more paragraph text</p>
  </div>
</template>

<script>
export default {
  middleware: [
    'auth'
  ],
  head () {
    return {
      title: 'Dashboard'
    }
  }
}
</script>
