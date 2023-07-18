<script setup>
    const download = {
        'title': 'Download',
        'subTitle': 'Download The Latest Version Of Our App',
        'content': 'Diam dolor diam ipsum et tempor sit. Aliqu diam amet diam et eos labore. Clita erat ipsum et lorem et sit, sed stet no labore lorem sit clita duo justo eirmod magna dolore erat amet',
        'image': 'img/about.png',
    }

    const {title, subTitle, content, image} = download

    const downloadContent = [
        {
            'icon': 'fab fa-apple',
            'title': 'App Store',
            'content': 'Available On',
            'delayTime': '0.5s'
        },
        {
            'icon': 'fab fa-android',
            'title': 'Play Store',
            'content': 'Available On',
            'delayTime': '0.5s'
        }
    ]
</script>
<template>
    <!-- Download Start -->
    <div class="container-xxl py-5">
        <div class="container py-5 px-lg-5">
            <div class="row g-5 align-items-center">
                <div class="col-lg-6">
                    <img class="img-fluid wow fadeInUp" data-wow-delay="0.1s" :src="image">
                </div>
                <div class="col-lg-6 wow fadeInUp" data-wow-delay="0.3s">
                    <h5 class="text-primary-gradient fw-medium">{{ title }}</h5>
                    <h1 class="mb-4">{{  subTitle }}</h1>
                    <p class="mb-4">{{ content }}</p>
                    <div class="row g-4">
                        <div v-for="(downloadData, index) in downloadContent" class="col-sm-6 wow fadeIn" :data-wow-delay="downloadData.delayTime" :key="index">
                            <a href="" class="d-flex bg-primary-gradient rounded py-3 px-4">
                                <i class="fa-3x text-white flex-shrink-0" :class="download.icon"></i>
                                <div class="ms-3">
                                    <p class="text-white mb-0">{{ downloadData.content  }}</p>
                                    <h5 class="text-white mb-0">{{ downloadData.title  }}</h5>
                                </div>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Download End -->
</template>
<style></style>