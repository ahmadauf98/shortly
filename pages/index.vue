<template>
  <div>
    <div id="section1" class="d-flex align-items-center">
      <section1 />
    </div>
    <div id="section2" class="d-flex align-items-center">
      <section2 />
    </div>
    <div id="section3" class="d-flex align-items-center">
      <section3 />
    </div>
  </div>
</template>

<script>
import section1 from '~/components/pages/section1.vue'
import section2 from '~/components/pages/section2.vue'
import section3 from '~/components/pages/section3.vue'
export default {
  components: {
    section1,
    section2,
    section3,
  },
}
</script>

<style scoped>
/* Small devices (mobile, 280px and up) */
@media only screen and (min-width: 280px) {
  #section1 {
    background-color: #fffffe;
    min-height: 100vh;
  }

  #section2 {
    background-color: #eff1f7;
    min-height: 90vh;
  }

  #section3 {
    background-image: url(~static/bg-boost-mobile.svg);
    background-color: #3b3054;
    background-repeat: no-repeat;
    background-size: 150%;
  }
}

/* Medium devices (tablet, 768px and up) */
@media only screen and (min-width: 768px) {
  #section1 {
    background-color: #fffffe;
    min-height: 70vh;
    padding: 0px 30px;
  }

  #section2 {
    background-color: #eff1f7;
    min-height: 85vh;
  }
}

/* Large devices (Laptop, 992px and up) */
@media only screen and (min-width: 992px) {
  #section1 {
    background-color: #fffffe;
    min-height: 100vh;
  }

  #section2 {
    background-color: #eff1f7;
    min-height: 85vh;
  }

  #section3 {
    background-image: url(~static/bg-boost-desktop.svg);
    background-color: #3b3054;
    background-repeat: no-repeat;
    background-size: 130%;
  }
}
</style>
