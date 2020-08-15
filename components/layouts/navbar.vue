<template>
  <div class="container-lg py-0 px-3 px-md-5 px-lg-0">
    <b-navbar toggleable="lg" class="px-0">
      <b-navbar-brand href="#">
        <img src="~/static/logo.svg" alt="..." />
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav v-for="nav in navbar" :key="nav.name">
          <b-nav-item class="nav-item mx-lg-2" :href="nav.href">{{
            nav.name
          }}</b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item class="nav-item mx-lg-2 mr-lg-4" href="#"
            >Login</b-nav-item
          >
          <b-nav-item class="nav-item mx-lg-2 d-flex d-lg-none" href="#">
            Sign Up
          </b-nav-item>
          <b-button class="custom-btn d-none d-lg-flex" size="md">
            Sign Up
          </b-button>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navbar: [
        { name: 'Features', href: '#' },
        { name: 'Pricing', href: '#' },
        { name: 'Resources', href: '#' },
      ],
    }
  },
}
</script>

<style scoped>
.nav-item {
  font-weight: 700;
}

.custom-btn {
  background-color: #2acfcf;
  border: none;
  border-radius: 50px;
  font-weight: 700;
  padding: 7px 25px;
}

.custom-btn:hover {
  background-color: #89d6d6;
  border: none;
  border-radius: 50px;
  font-weight: 700;
  padding: 7px 25px;
}
</style>
