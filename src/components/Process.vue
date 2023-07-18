<script setup>
    const process = {
        'title': 'How It Works',
        'subTitle': '3 Easy Steps',
        
    }
    const {title, subTitle} = process

    const processContent = [
        {
            'icon': 'fa fa-cog',
            'title': 'Install the App',
            'delayTime': '0.1s',
            'content': 'Tempor erat elitr rebum clita dolor diam ipsum sit diam amet diam eos erat ipsum et lorem et sit sed stet',
        },
        {
            'icon': 'fa fa-address-card',
            'title': 'Setup Your Profile',
            'delayTime': '0.3s',
            'content': 'Tempor erat elitr rebum clita dolor diam ipsum sit diam amet diam eos erat ipsum et lorem et sit sed stet',
        },
        {
            'icon': 'fa fa-check',
            'title': 'Enjoy The Features',
            'delayTime': '0.5s',
            'content': 'Tempor erat elitr rebum clita dolor diam ipsum sit diam amet diam eos erat ipsum et lorem et sit sed stet',
        }
    ]
</script>
<template>
    <!-- Process Start -->
    <div class="container-xxl py-5">
        <div class="container py-5 px-lg-5">
            <div class="text-center pb-4 wow fadeInUp" data-wow-delay="0.1s">
                <h5 class="text-primary-gradient fw-medium">{{ title }}</h5>
                <h1 class="mb-5">{{ subTitle }}</h1>
            </div>
            <div class="row gy-5 gx-4 justify-content-center">
                <div v-for="(procesData, index) in processContent" class="col-lg-4 col-sm-6 text-center pt-4 wow fadeInUp" :data-wow-delay="procesData.delayTime" :key="index">
                    <div class="position-relative bg-light rounded pt-5 pb-4 px-4">
                        <div class="d-inline-flex align-items-center justify-content-center bg-primary-gradient rounded-circle position-absolute top-0 start-50 translate-middle shadow" style="width: 100px; height: 100px;">
                            <i class="fa-3x text-white" :class="procesData.icon"></i>
                        </div>
                        <h5 class="mt-4 mb-3">{{ procesData.title }}</h5>
                        <p class="mb-0">{{ procesData.content }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Process Start -->
</template>
<style></style>