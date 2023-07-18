<script setup>
    const logo = {
        'siteLogo': 'MyApp',
        'trail': 'Start Free Trial',
        'link': '#',
        'linkText': 'Read More',
        'title': 'The Revolutionary App That Helps To Control Your Own Fitness',
        'contact': 'Contact us',
        'content': 'Tempor rebum no at dolore lorem clita rebum rebum ipsum rebum stet dolor sed justo kasd. Ut dolor sed magna dolor sea diam. Sit diam sit justo amet ipsum vero ipsum clita lorem'
    }

    const { siteLogo, trail, link, linkText, title, contact, content } = logo

    const navItems = [
        {
            'id': 1,
            'title': 'Home',
            'link': '#home'
        },
        {
            'id': 2,
            'title': 'About',
            'link': '#about'
        },
        {
            'id': 3,
            'title': 'Feature',
            'link': '#feature'
        },
        {
            'id': 4,
            'title': 'Pricing',
            'link': '#pricing'
        },
        {
            'id': 5,
            'title': 'Review',
            'link': '#review'
        },
        {
            'id': 6,
            'title': 'Contact',
            'link': '#contact'
        }
    ]


    const sliderImages = [
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

    <!-- Navbar & Hero Start -->
    <div class="container-xxl position-relative p-0" id="home">
            <nav class="navbar navbar-expand-lg navbar-light px-4 px-lg-5 py-3 py-lg-0">
                <a href="" class="navbar-brand p-0">
                    <h1 class="m-0">{{ siteLogo }}</h1>
                    <!-- <img src="img/logo.png" alt="Logo"> -->
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarCollapse">
                    <span class="fa fa-bars"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarCollapse">
                    <div class="navbar-nav mx-auto py-0">
                        <a v-for="navItem in navItems" :key="navItem.id" :href="navItem.link" class="nav-item nav-link">{{ navItem.title }}</a>
                    </div>
                    <a :href="link" class="btn btn-primary-gradient rounded-pill py-2 px-4 ms-3 d-none d-lg-block">{{ trail }}</a>
                </div>
            </nav>

            <div class="container-xxl bg-primary hero-header">
                <div class="container px-lg-5">
                    <div class="row g-5">
                        <div class="col-lg-8 text-center text-lg-start">
                            <h1 class="text-white mb-4 animated slideInDown">{{ title }}</h1>
                            <p class="text-white pb-3 animated slideInDown">{{ content }}</p>
                            <a :href="link" class="btn btn-primary-gradient py-sm-3 px-4 px-sm-5 rounded-pill me-3 animated slideInLeft">{{ linkText }}</a>
                            <a href="" class="btn btn-secondary-gradient py-sm-3 px-4 px-sm-5 rounded-pill animated slideInRight">{{ contact }}</a>
                        </div>
                        <div class="col-lg-4 d-flex justify-content-center justify-content-lg-end wow fadeInUp" data-wow-delay="0.3s">
                            <div class="owl-carousel screenshot-carousel">
                                <img v-for=" (sliderImage, index) in sliderImages" :key="index" class="img-fluid" :src="sliderImage.image" :alt="sliderImage.alt">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Navbar & Hero End -->
</template>
<style></style>