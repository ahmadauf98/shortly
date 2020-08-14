<template>
  <div>
    <div id="Navbar">
      <Navbar />
    </div>
    <div id="Body">
      <Nuxt />
    </div>
  </div>
</template>

<script>
import Navbar from '~/components/layouts/navbar.vue'
export default {
  components: {
    Navbar,
  },
}
</script>

<style>
#Navbar {
  background-color: #fffffe;
  padding: 1em 0em;
}

#Body{
  overflow-x: hidden;
}
</style>
