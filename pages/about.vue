<template>
    <div>
        <h1>About Page</h1>
    </div>
</template>

<script>
export default {
     head: {
    titleTemplate: 'My Nuxt JS App - About',
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },

      // hid is used as unique identifier. Do not use `vmid` for it as it will not work
      { hid: 'description', name: 'description', content: 'About Nuxt JS app' }
    ]
  }
}
</script>

<style>

</style>
