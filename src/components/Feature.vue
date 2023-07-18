<script setup>
    const featureContent = {
        'title': 'About Features',
        'subTitle': 'Awesome Features',
    }
    const {title, subTitle} = featureContent

    const features = [
        {
            'icon': 'fa fa-eye',
            'title': 'High Resolution',
            'content': 'Erat ipsum justo amet duo et elitr dolor, est duo duo eos lorem sed diam stet diam sed stet lorem.',
            'delayTime': '0.1s'
        },
        {
            'icon': 'fa fa-layer-group',
            'title': 'Retina Ready',
            'content': 'Erat ipsum justo amet duo et elitr dolor, est duo duo eos lorem sed diam stet diam sed stet lorem.',
            'delayTime': '0.3s'
        },

        {
            'icon': 'fa fa-edit',
            'title': 'Editable Data',
            'content': 'Erat ipsum justo amet duo et elitr dolor, est duo duo eos lorem sed diam stet diam sed stet lorem.',
            'delayTime': '0.5s'
        },

        {
            'icon': 'fa fa-shield-alt',
            'title': 'Fully Secured',
            'content': 'Erat ipsum justo amet duo et elitr dolor, est duo duo eos lorem sed diam stet diam sed stet lorem.',
            'delayTime': '0.1s'
        },

        {
            'icon': 'fa fa-shield-alt',
            'title': 'Cloud Storage',
            'content': 'Erat ipsum justo amet duo et elitr dolor, est duo duo eos lorem sed diam stet diam sed stet lorem.',
            'delayTime': '0.1s'
        },

        {
            'icon': 'fa fa-mobile-alt',
            'title': 'Fully Responsive',
            'content': 'Erat ipsum justo amet duo et elitr dolor, est duo duo eos lorem sed diam stet diam sed stet lorem.',
            'delayTime': '0.5s'
        },
    ]
</script>

<template>

    <!-- Features Start -->
    <div class="container-xxl py-5" id="feature">
        <div class="container py-5 px-lg-5">
            <div class="text-center wow fadeInUp" data-wow-delay="0.1s">
                <h5 class="text-primary-gradient fw-medium">{{ title }}</h5>
                <h1 class="mb-5">{{ subTitle }}</h1>
            </div>
            <div class="row g-4">
                <div v-for="(feature, index) in features" class="col-lg-4 col-md-6 wow fadeInUp" :data-wow-delay="feature.delayTime" :key="index">
                    <div class="feature-item bg-light rounded p-4">
                        <div class="d-inline-flex align-items-center justify-content-center bg-primary-gradient rounded-circle mb-4" style="width: 60px; height: 60px;">
                            <i class="text-white fs-4" :class="feature.icon"></i>
                        </div>
                        <h5 class="mb-3">{{ feature.title }}</h5>
                        <p class="m-0">{{ feature.content }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Features End -->
</template>

<style scoped>

</style>