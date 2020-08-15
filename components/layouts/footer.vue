<template>
  <div class="container py-5 px-3">
    <div class="row pt-3">
      <div class="col-12 col-lg-3 text-center text-lg-left mb-5 mb-lg-0">
        <div class="brand-logo" id="brand-logo">
          <img src="~/static/logo-white.svg" alt="..." />
        </div>
      </div>
      <div class="col-12 col-lg-2 text-center text-lg-left mb-4 mb-lg-0">
        <h5 class="link-header mb-3">Features</h5>
        <div
          class="d-block mb-2"
          v-for="feature in features"
          :key="feature.name"
        >
          <a class="link-style" :href="feature.href">{{ feature.name }}</a>
        </div>
      </div>
      <div class="col-12 col-lg-2 text-center text-lg-left mb-4 mb-lg-0">
        <h5 class="link-header mb-3">Resources</h5>
        <div
          class="d-block mb-2"
          v-for="resource in resources"
          :key="resource.name"
        >
          <a class="link-style" :href="resource.href">{{ resource.name }}</a>
        </div>
      </div>
      <div class="col-12 col-lg-2 text-center text-lg-left mb-4 mb-lg-0">
        <h5 class="link-header mb-3">Company</h5>
        <div
          class="d-block mb-2"
          v-for="company in companies"
          :key="company.name"
        >
          <a class="link-style" :href="company.href">{{ company.name }}</a>
        </div>
      </div>
      <div class="col-12 col-lg-3 text-center">
        <div class="d-inline" v-for="social in socials" :key="social.name">
          <a class="mx-3" href="#"> <img :src="social.logo" alt="..." /></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      features: [
        {
          name: 'Link Shortening',
          href: '#',
        },
        {
          name: 'Branded Links',
          href: '#',
        },
        {
          name: 'Analytics',
          href: '#',
        },
      ],
      resources: [
        {
          name: 'Blog',
          href: '#',
        },
        {
          name: 'Developers',
          href: '#',
        },
        {
          name: 'Support',
          href: '#',
        },
      ],
      companies: [
        {
          name: 'About',
          href: '#',
        },
        {
          name: 'Our Team',
          href: '#',
        },
        {
          name: 'Careers',
          href: '#',
        },
        {
          name: 'Contact ',
          href: '#',
        },
      ],
      socials: [
        { name: 'facebook', logo: 'icon-facebook.svg' },
        {
          name: 'twitter',
          logo: 'icon-twitter.svg',
        },
        {
          name: 'pinterest',
          logo: 'icon-pinterest.svg',
        },
        {
          name: 'instagram',
          logo: 'icon-instagram.svg',
        },
      ],
    }
  },
}
</script>

<style scoped>
.link-header {
  color: white;
  font-weight: 700;
}

.link-style {
  color: grey;
  font-weight: 500;
  text-decoration: none;
}

.link-style:hover {
  color: white;
  font-weight: 500;
  text-decoration: none;
}
</style>
