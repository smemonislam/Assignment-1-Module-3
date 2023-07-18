<script setup>

  const aboutContent = {
    'title': 'About App',
    'subTitle': '#1 App For Your Fitness',
    'btnText': 'Read More',
    'link': 'index.html',
    'image': 'img/about.png',
    'content': 'Diam dolor diam ipsum et tempor sit. Aliqu diam amet diam et eos labore. Clita erat ipsum et lorem et sit, sed stet no labore lorem sit clita duo justo eirmod magna dolore erat amet',
  }

  const {title, subTitle, content, btnText, link, image} = aboutContent

  const clientReviews = [
    {
      'icon': 'fa fa-cogs fa-2x text-primary-gradient',
      'activeNumber': '1234',
      'activeContent': 'Active Install',
      'delayTime': '0.1s'
    },
    {
      'icon': 'fa fa-comments fa-2x text-secondary-gradient',
      'activeNumber': '1234',
      'activeContent': 'Clients Reviews',
      'delayTime': '0.7s'
    }
  ]


</script>

<template>
  <!-- About Start -->
  <div class="container-xxl py-5" id="about">
    <div class="container py-5 px-lg-5">
        <div class="row g-5 align-items-center">
            <div class="col-lg-6 wow fadeInUp" data-wow-delay="0.1s">
                <h5 class="text-primary-gradient fw-medium">{{ title }}</h5>
                <h1 class="mb-4">{{ subTitle }}</h1>
                <p class="mb-4">{{ content }}</p>
                <div class="row g-4 mb-4">
                    <div v-for="(clientReview, index) in clientReviews" class="col-sm-6 wow fadeIn" :data-wow-delay="clientReview.icon" :key="index">
                        <div class="d-flex">
                            <i class="flex-shrink-0 mt-1" :class="clientReview.icon"></i>
                            <div class="ms-3">
                                <h2 class="mb-0" data-toggle="counter-up">{{ clientReview.activeNumber }}</h2>
                                <p class="text-primary-gradient mb-0">{{ clientReview.activeContent }}</p>
                            </div>
                        </div>
                    </div>
                </div>
                <a :href="link" class="btn btn-primary-gradient py-sm-3 px-4 px-sm-5 rounded-pill mt-3">{{ btnText }}</a>
            </div>
            <div class="col-lg-6">
              <img class="img-fluid wow fadeInUp" data-wow-delay="0.5s" :src="image">
            </div>
        </div>
    </div>
</div>
<!-- About End -->
</template>

<style scoped>
</style>
