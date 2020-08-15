<template>
  <div
    class="container p-5 px-3 d-flex align-items-center justify-content-center"
  >
    <div class="row text-center">
      <div id="title" class="col-12 mb-4">
        <h1 class="text-white font-weight-bold">{{ title }}</h1>
      </div>
      <div id="button" class="col-12">
        <b-button class="custom-btn" size="md">
          Get Started
        </b-button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Boost your links today',
    }
  },
}
</script>

<style scoped>
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

.text-white {
  color: white;
}
</style>
