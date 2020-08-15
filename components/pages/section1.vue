<template>
  <div class="container-lg py-0 px-3 mb-lg-5">
    <div class="row d-flex align-items-center mb-lg-5">
      <div
        class="col-12 col-lg-6 d-flex d-lg-none d-flex justify-content-center"
      >
        <img
          class="illustration"
          src="~/static/illustration-working-mobile.svg"
          alt="..."
        />
      </div>
      <div class="col-12 col-lg-6">
        <div id="title" class="mb-3 mb-lg-2">
          <h1
            class="display-4 font-weight-bolder text-color text-center text-lg-left"
          >
            {{ title }}
          </h1>
        </div>
        <div id="subtitle" class="mb-4">
          <h3 class="lead pr-lg-5 text-center text-lg-left">{{ subtitle }}</h3>
        </div>
        <div id="button" class="text-center text-lg-left mb-5 mb-lg-0">
          <b-button class="custom-btn" size="md">
            Get Started
          </b-button>
        </div>
      </div>
      <div class="col-12 col-lg-6 d-none d-lg-flex">
        <img src="~/static/illustration-working.svg" alt="..." />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'More than just shorter links',
      subtitle:
        "Build your brand's recognition and get detailed insights on how your links are performing.",
    }
  },
}
</script>

<style scoped>
.text-color {
  color: #232127;
}

.custom-btn {
  background-color: #2acfcf;
  border: none;
  border-radius: 50px;
  font-weight: 700;
  padding: 10px 30px;
}

.custom-btn:hover {
  background-color: #89d6d6;
  border: none;
  border-radius: 50px;
  font-weight: 700;
  padding: 10px 30px;
}

/* Small devices (mobile, 320px and up) */
@media only screen and (max-width: 767px) {
  .illustration {
    width: 400px;
    margin-bottom: 3em;
  }

  .display-4 {
    font-size: 45px;
  }
}

/* Medium devices (tablet, 768px to 991px) */
@media only screen and (min-width: 768px) and (max-width: 991px) {
  .illustration {
    width: 500px;
    margin-bottom: 3em;
  }

  .display-4 {
    font-size: 45px;
  }
}
</style>
