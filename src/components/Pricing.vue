<script setup>
    const download = {
        'title': 'Pricing Plan',
        'subTitle': 'Choose Your Plan',
    }

    const {title, subTitle, content, image} = download

    const navTitle = [
        {
            'id': 1,
            'title': 'Monthly',
            'link': '#tab-1'
        },
        {
            'id': 2,
            'title': 'Yearly',
            'link': '#tab-2'
        }
    ]

    const navItemsMonthly = [
        {
            'id': 1,
            'title': 'Starter Plan',
            'subTitle': 'Powerful & Awesome Features',
            'currency': '$',
            'price': 14.99,
            'year': 'Yearly',
            'content1': 'HTML5 & CSS3',
            'content2': 'Bootstrap v5',
            'content3': 'Responsive Layout',
            'content4': 'Cross-browser Support',
            'content5': 'Get Started',
            'link': '#',
        },
        {
            'id': 2,
            'title': 'Advance Plan',
            'subTitle': 'Powerful & Awesome Features',
            'currency': '$',
            'price': 24.99,
            'year': 'Yearly',
            'content1': 'HTML5 & CSS3',
            'content2': 'Bootstrap v5',
            'content3': 'Responsive Layout',
            'content4': 'Cross-browser Support',
            'content5': 'Get Started',
            'link': '#',
        },
        {
            'id': 3,
            'title': 'Premium Plan',
            'subTitle': 'Powerful & Awesome Features',
            'currency': '$',
            'price': 34.99,
            'year': 'Yearly',
            'content1': 'HTML5 & CSS3',
            'content2': 'Bootstrap v5',
            'content3': 'Responsive Layout',
            'content4': 'Cross-browser Support',
            'content5': 'Get Started',
            'link': '#',
        }
    ]

    const navItemsYearly = [
        {
            'id': 1,
            'title': 'Starter Plan',
            'subTitle': 'Powerful & Awesome Features',
            'currency': '$',
            'price': 114.99,
            'month': 'Month',
            'content1': 'HTML5 & CSS3',
            'content2': 'Bootstrap v5',
            'content3': 'Responsive Layout',
            'content4': 'Cross-browser Support',
            'content5': 'Get Started',
            'link': '#',
        },
        {
            'id': 2,
            'title': 'Advance Plan',
            'subTitle': 'Powerful & Awesome Features',
            'currency': '$',
            'price': 124.99,
            'month': 'Month',
            'content1': 'HTML5 & CSS3',
            'content2': 'Bootstrap v5',
            'content3': 'Responsive Layout',
            'content4': 'Cross-browser Support',
            'content5': 'Get Started',
            'link': '#',
        },
        {
            'id': 3,
            'title': 'Premium Plan',
            'subTitle': 'Powerful & Awesome Features',
            'currency': '$',
            'price': 134.99,
            'month': 'Month',
            'content1': 'HTML5 & CSS3',
            'content2': 'Bootstrap v5',
            'content3': 'Responsive Layout',
            'content4': 'Cross-browser Support',
            'content5': 'Get Started',
            'link': '#',
        }
    ]
</script>
<template>
    <!-- Pricing Start -->
    <div class="container-xxl py-5" id="pricing">
        <div class="container py-5 px-lg-5">
            <div class="text-center wow fadeInUp" data-wow-delay="0.1s">
                <h5 class="text-primary-gradient fw-medium">{{ title  }}</h5>
                <h1 class="mb-5">{{ subTitle }}</h1>
            </div>
            <div class="tab-class text-center pricing wow fadeInUp" data-wow-delay="0.1s">
                <ul class="nav nav-pills d-inline-flex justify-content-center bg-primary-gradient rounded-pill mb-5">
                    <li class="nav-item" v-for="navItem in navTitle" :key="navItem.id">
                        <button class="nav-link" data-bs-toggle="pill" :href="navItem.link">{{ navItem.title }}</button>
                    </li>
                </ul>
                <div class="tab-content text-start">
                    <div id="tab-1" class="tab-pane fade show p-0 active">
                        <div class="row g-4">
                            <div class="col-lg-4" v-for="navItemMonthly in navItemsMonthly" :key="navItemMonthly.id">
                                <div class="bg-light rounded">
                                    <div class="border-bottom p-4 mb-4">
                                        <h4 class="text-primary-gradient mb-1">{{ navItemMonthly.title }}</h4>
                                        <span>{{ navItemMonthly.subTitle }}</span>
                                    </div>
                                    <div class="p-4 pt-0">
                                        <h1 class="mb-3">
                                            <small class="align-top" style="font-size: 22px; line-height: 45px;">{{ navItemMonthly.currency }}</small>{{ navItemMonthly.price }}<small
                                                class="align-bottom" style="font-size: 16px; line-height: 40px;">/ {{ navItemMonthly.year }}</small>
                                        </h1>
                                        <div class="d-flex justify-content-between mb-3"><span>{{ navItemMonthly.content1 }}</span><i class="fa fa-check text-primary-gradient pt-1"></i></div>
                                        <div class="d-flex justify-content-between mb-3"><span>{{ navItemMonthly.content2 }}</span><i class="fa fa-check text-primary-gradient pt-1"></i></div>
                                        <div class="d-flex justify-content-between mb-3"><span>{{ navItemMonthly.content3 }}</span><i class="fa fa-check text-primary-gradient pt-1"></i></div>
                                        <div class="d-flex justify-content-between mb-2"><span>{{ navItemMonthly.content4 }}</span><i class="fa fa-check text-primary-gradient pt-1"></i></div>
                                        <a :href="navItemMonthly.link" class="btn btn-primary-gradient rounded-pill py-2 px-4 mt-4">{{ navItemMonthly.content5 }}</a>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div id="tab-2" class="tab-pane fade p-0">
                        <div class="row g-4">
                            <div class="col-lg-4" v-for="navItemYearly in navItemsYearly" :key="navItemYearly.id">
                                <div class="bg-light rounded">
                                    <div class="border-bottom p-4 mb-4">
                                        <h4 class="text-primary-gradient mb-1">{{ navItemYearly.title }}</h4>
                                        <span>{{ navItemYearly.subTitle }}</span>
                                    </div>
                                    <div class="p-4 pt-0">
                                        <h1 class="mb-3">
                                            <small class="align-top" style="font-size: 22px; line-height: 45px;">{{ navItemYearly.currency }}</small>{{ navItemYearly.price }}<small
                                                class="align-bottom" style="font-size: 16px; line-height: 40px;">/ {{ navItemYearly.month }}</small>
                                        </h1>
                                        <div class="d-flex justify-content-between mb-3"><span>{{ navItemYearly.content1 }}</span><i class="fa fa-check text-primary-gradient pt-1"></i></div>
                                        <div class="d-flex justify-content-between mb-3"><span>{{ navItemYearly.content2 }}</span><i class="fa fa-check text-primary-gradient pt-1"></i></div>
                                        <div class="d-flex justify-content-between mb-3"><span>{{ navItemYearly.content3 }}</span><i class="fa fa-check text-primary-gradient pt-1"></i></div>
                                        <div class="d-flex justify-content-between mb-2"><span>{{ navItemYearly.content4 }}</span><i class="fa fa-check text-primary-gradient pt-1"></i></div>
                                        <a :href="navItemYearly.link" class="btn btn-primary-gradient rounded-pill py-2 px-4 mt-4">{{ navItemYearly.content5 }}</a>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Pricing End -->
</template>
<style></style>