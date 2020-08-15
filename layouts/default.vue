<template>
  <div>
    <div id="Navbar">
      <Navbar />
    </div>
    <div id="Body">
      <Nuxt />
    </div>
    <div id="Footer">
      <Footer />
    </div>
  </div>
</template>

<script>
import Navbar from '~/components/layouts/navbar.vue'
import Footer from '~/components/layouts/footer.vue'
export default {
  components: {
    Navbar,
    Footer,
  },
}
</script>

<style>
#Navbar {
  background-color: #fffffe;
  padding: 1em 0em;
}

#Body {
  overflow-x: hidden;
}

#Footer {
  background-color: #232127;
}

.lead {
  font-weight: 500;
  font-size: 18px;
  line-height: 25px;
  color: #9e9aa7;
}
</style>
