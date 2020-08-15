<template>
  <div class="container py-0 pb-5 px-3">
    <div class="row px-3">
      <!-- Desktop Shorten -->
      <div
        class="card-custom col-12 d-none d-lg-flex align-items-center justify-content-center"
      >
        <b-form inline>
          <b-input
            class="input-custom mr-3"
            placeholder="Shorten a link here..."
          ></b-input>

          <b-button class="custom-btn">Shorten It!</b-button>
        </b-form>
      </div>
      <!-- Mobile Shorten -->
      <div
        class="card-custom-mobile my-5 text-center col-12 d-flex d-lg-none align-items-center justify-content-center"
      >
        <b-form>
          <b-input
            class="input-custom mb-3"
            placeholder="Shorten a link here..."
          ></b-input>

          <b-button class="custom-btn-mobile btn-block">Shorten It!</b-button>
        </b-form>
      </div>
    </div>
    <div class="row d-block">
      <div id="title" class="text-center mb-3 d-flex justify-content-center">
        <div class="col-12 col-lg-6">
          <h1 class="font-weight-bolder text-color">{{ title }}</h1>
        </div>
      </div>

      <div id="subtitle" class="text-center mb-5 d-flex justify-content-center">
        <div class="col-12 col-lg-6 mb-3">
          <h3 class="lead">{{ subtitle }}</h3>
        </div>
      </div>
      <div id="card-info" class="row">
        <div
          class="col-12 col-lg-4 mb-4 mb-lg-0 text-center text-lg-left"
          v-for="card in cards"
          :key="card.title"
        >
          <b-card class="card">
            <b-avatar class="avatar" size="5rem">
              <img :src="card.img" alt="..." />
            </b-avatar>

            <b-card-title class="h4 font-weight-bold text-color">
              {{ card.title }}
            </b-card-title>
            <b-card-text class="custom-lead">
              {{ card.subtitle }}
            </b-card-text>
          </b-card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Advanced Statistics',
      subtitle:
        'Track how your links are performing across the web with our advances statistics dashboard.',
      cards: [
        {
          img: 'icon-brand-recognition.svg',
          title: 'Brand Recognition',
          subtitle:
            "Boost your recognition with each click. Generic links don't mean a thing. Branded links help instil confidence in your content.",
        },
        {
          img: 'icon-detailed-records.svg',
          title: 'Detailed Records',
          subtitle:
            'Gain insights into who is clicking your links. Knowing when and where people engage with your content helps inform better decisions.',
        },
        {
          img: 'icon-fully-customizable.svg',
          title: 'Fully Customizable',
          subtitle:
            'Improve brand awareness and content discoverability through customizable links, supercharging audience engagement.',
        },
      ],
    }
  },
}
</script>

<style scoped>
::placeholder {
  color: #9e9aa7;
  opacity: 1; /* Firefox */
}

:-ms-input-placeholder {
  /* Internet Explorer 10-11 */
  color: #9e9aa7;
}

::-ms-input-placeholder {
  /* Microsoft Edge */
  color: #9e9aa7;
}

.text-color {
  color: #232127;
}

.custom-lead {
  font-weight: 400;
  font-size: 17px;
  line-height: 25px;
  color: #9e9aa7;
}
/* Small devices (mobile, 280px and up) */
@media only screen and (min-width: 280px) {
  .card-custom-mobile {
    background-color: #3b3054;
    background-image: url(~static/bg-shorten-mobile.svg);
    background-size: 80%;
    background-repeat: no-repeat;
    background-position: right top;
    height: 170px;
    border-radius: 15px;
  }

  .card {
    border: none;
    background-color: white;
    padding: 10px;
    margin: 1.5em;
  }

  .avatar {
    background-color: #3b3054;
    bottom: 85px;
    margin-bottom: -70px;
  }

  .input-custom {
    padding: 21px 30px;
    color: #9e9aa7;
    min-width: 220px;
    font-weight: 700;
  }

  .custom-btn-mobile {
    background-color: #2acfcf;
    border: none;
    font-weight: 700;
    min-width: 220px;
    padding: 10px 30px;
  }

  .custom-btn-mobile:hover {
    background-color: #89d6d6;
    border: none;
    font-weight: 700;
    min-width: 220px;
    padding: 10px 30px;
  }
}

/* Medium devices (tablet, 768px and up) */
@media only screen and (min-width: 768px) {
   .input-custom {
    padding: 21px 30px;
    color: #9e9aa7;
    min-width: 600px;
    font-weight: 700;
  }
}

/* Large devices (Laptop, 992px and up) */
@media only screen and (min-width: 992px)and (max-width: 1919px){
  .card-custom {
    background-color: #3b3054;
    background-image: url(~static/bg-shorten-desktop.svg);
    background-size: 100%;
    background-repeat: no-repeat;
    background-position: center;
    height: 170px;
    border-radius: 15px;
    margin-top: -7%;
    margin-bottom: 5%;
  }

  .card {
    border: none;
    background-color: white;
    padding: 15px;
  }

  .avatar {
    background-color: #3b3054;
    bottom: 95px;
    margin-bottom: -80px;
  }

  .input-custom {
    padding: 21px 30px;
    color: #9e9aa7;
    width: 700px;
    font-weight: 700;
  }

  .custom-btn {
    background-color: #2acfcf;
    border: none;
    font-weight: 700;
    padding: 10px 30px;
  }

  .custom-btn:hover {
    background-color: #89d6d6;
    border: none;
    font-weight: 700;
    padding: 10px 30px;
  }
}

/* Large devices (Desktop, 1920px and up) */
@media only screen and (min-width: 1920px) {
  .card-custom {
    background-color: #3b3054;
    background-image: url(~static/bg-shorten-desktop.svg);
    background-size: 100%;
    background-repeat: no-repeat;
    background-position: center;
    height: 170px;
    border-radius: 15px;
    margin-top: -20%;
    margin-bottom: 8%;
  }

  .card {
    border: none;
    background-color: white;
    padding: 15px;
  }

  .avatar {
    background-color: #3b3054;
    bottom: 95px;
    margin-bottom: -80px;
  }

  .input-custom {
    padding: 21px 30px;
    color: #9e9aa7;
    width: 700px;
    font-weight: 700;
  }

  .custom-btn {
    background-color: #2acfcf;
    border: none;
    font-weight: 700;
    padding: 10px 30px;
  }

  .custom-btn:hover {
    background-color: #89d6d6;
    border: none;
    font-weight: 700;
    padding: 10px 30px;
  }
}
</style>
