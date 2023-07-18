<script setup>

    const screenshot = {
        'title': 'Screenshot',
        'subTitle': 'User Friendly interface And Very Easy To Use Fitness App',
        'content': 'Diam dolor diam ipsum et tempor sit. Aliqu diam amet diam et eos labore. Clita erat ipsum et lorem et sit, sed stet no labore lorem sit clita duo justo eirmod magna dolore erat amet',
        'btnText': 'Read More',
        'link': 'index.html'
    }
    const {title, subTitle, content, btnText, link} = screenshot

    const screenshotLoops = [
        {
            'content': 'Diam dolor diam ipsum et tempor sit',
        },
        {
            'content': 'Aliqu diam amet diam et eos labore'
        },
        {
            'content': 'Clita erat ipsum et lorem et sit'
        }
    ]

    const screenshotImages = [
        {
            'image': 'img/screenshot-1.png',
            'alt': 'No Image Found!'
        },
        {
            'image': 'img/screenshot-2.png',
            'alt': 'No Image Found!'
        },
        {
            'image': 'img/screenshot-3.png',
            'alt': 'No Image Found!'
        },
        {
            'image': 'img/screenshot-4.png',
            'alt': 'No Image Found!'
        },
        {
            'image': 'img/screenshot-5.png',
            'alt': 'No Image Found!'
        }
    ]
</script>
<template>
    <!-- Screenshot Start -->
    <div class="container-xxl py-5">
        <div class="container py-5 px-lg-5">
            <div class="row g-5 align-items-center">
                <div class="col-lg-8 wow fadeInUp" data-wow-delay="0.1s">
                    <h5 class="text-primary-gradient fw-medium">{{ title }}</h5>
                    <h1 class="mb-4">{{ subTitle }}</h1>
                    <p class="mb-4">{{ content }}</p>
                    <p v-for="(screenshotLoop, index) in screenshotLoops" :key="index"><i class="fa fa-check text-primary-gradient me-3"></i>{{ screenshotLoop.content }}</p>
                    <a :href="link" class="btn btn-primary-gradient py-sm-3 px-4 px-sm-5 rounded-pill mt-3 mt-4">{{ btnText }}</a>
                </div>
                <div class="col-lg-4 d-flex justify-content-center justify-content-lg-end wow fadeInUp" data-wow-delay="0.3s">
                    <div class="owl-carousel screenshot-carousel">
                        <img class="img-fluid" v-for="(screenshotImage, index) in screenshotImages" :key="index" :src="screenshotImage.image" :alt="screenshotImage.alt">
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Screenshot End -->
</template>
<style></style>