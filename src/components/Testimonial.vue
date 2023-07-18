<script setup>
    const testimonial = {
        'title': 'Testimonial',
        'subTitle': 'What Say Our Clients!'
    }

    const {title, subTitle} = testimonial

    const carouselItems = [
        {
            'id': 1,
            'title': 'Client Name',
            'content': 'Profession',
            'image': 'img/testimonial-1.jpg',
            'description': 'Tempor erat elitr rebum at clita. Diam dolor diam ipsum sit diam amet diam et eos. Clita erat ipsum et lorem et sit.'
        },
        {
            'id': 2,
            'title': 'Client Name',
            'content': 'Profession',
            'image': 'img/testimonial-2.jpg',
            'description': 'Tempor erat elitr rebum at clita. Diam dolor diam ipsum sit diam amet diam et eos. Clita erat ipsum et lorem et sit.'
        },
        {
            'id': 3,
            'title': 'Client Name',
            'content': 'Profession',
            'image': 'img/testimonial-3.jpg',
            'description': 'Tempor erat elitr rebum at clita. Diam dolor diam ipsum sit diam amet diam et eos. Clita erat ipsum et lorem et sit.'
        },
        {
            'id': 4,
            'title': 'Client Name',
            'content': 'Profession',
            'image': 'img/testimonial-4.jpg',
            'description': 'Tempor erat elitr rebum at clita. Diam dolor diam ipsum sit diam amet diam et eos. Clita erat ipsum et lorem et sit.'
        }
    ]
</script>
<template>
    <!-- Testimonial Start -->
    <div class="container-xxl py-5" id="review">
        <div class="container py-5 px-lg-5">
            <div class="text-center wow fadeInUp" data-wow-delay="0.1s">
                <h5 class="text-primary-gradient fw-medium">{{ title }}</h5>
                <h1 class="mb-5">{{ subTitle }}</h1>
            </div>
            <div class="owl-carousel testimonial-carousel wow fadeInUp" data-wow-delay="0.1s">
                <div class="testimonial-item rounded p-4" v-for="carouselItem in carouselItems" :key="carouselItem.id">
                    <div class="d-flex align-items-center mb-4">
                        <img class="img-fluid bg-white rounded flex-shrink-0 p-1" :src="carouselItem.image" style="width: 85px; height: 85px;">
                        <div class="ms-4">
                            <h5 class="mb-1">{{ carouselItem.title }}</h5>
                            <p class="mb-1">{{ carouselItem.content }}</p>
                            <div>
                                <small class="fa fa-star text-warning"></small>
                                <small class="fa fa-star text-warning"></small>
                                <small class="fa fa-star text-warning"></small>
                                <small class="fa fa-star text-warning"></small>
                                <small class="fa fa-star text-warning"></small>
                            </div>
                        </div>
                    </div>
                    <p class="mb-0">{{ carouselItem.description }}</p>
                </div>
            </div>
        </div>
    </div>
    <!-- Testimonial End -->
</template>
<style></style>