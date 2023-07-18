<script setup>
    const widgets = {
        'wiget1': 'Address',
        'wiget2': 'Quick Link',
        'wiget3': 'Popular Link',
        'wiget4': 'Newsletter',
        'content': 'Lorem ipsum dolor sit amet elit. Phasellus nec pretium mi. Curabitur facilisis ornare velit non vulpu'
    }

    const {wiget1, wiget2, wiget3, wiget4, content} = widgets

    const infoWidgets = [
        {
            'id': 1,
            'title': '123 Street, New York, USA',
            'icon': 'fa fa-map-marker-alt'
        },
        {
            'id': 2,
            'title': '+012 345 67890',
            'icon': 'fa fa-phone-alt'
        },
        {
            'id': 3,
            'title': 'info@example.com',
            'icon': 'fa fa-envelope'
        }
    ]

    const socials = [
        {
            'id': 1,
            'link': '#',
            'icon': 'fa-twitter'
        },
        {
            'id': 2,
            'link': '#',
            'icon': 'fa-facebook-f'
        },
        {
            'id': 3,
            'link': '#',
            'icon': 'fab fa-instagram'
        },
        {
            'id': 4,
            'link': '#',
            'icon': 'fa-linkedin-in'
        }
    ]

    const menuItems = [
        {
            'id': 1,
            'title': 'About Us',
            'link': '#'
        },
        {
            'id': 2,
            'title': 'Contact Us',
            'link': '#'
        },
        {
            'id': 3,
            'title': 'Privacy Policy',
            'link': '#'
        },
        {
            'id': 4,
            'title': 'Terms & Condition',
            'link': '#'
        },
        {
            'id': 5,
            'title': 'Career',
            'link': '#'
        }
    ]

    const copyright = {
        'text': 'All Right Reserved. Designed By',
        'name': 'SM Emon Islam',
        'link': '#'
    }

    const {text, name, link} = copyright

    const menuItems2 = [
        {
            'id': 1,
            'title': 'Home',
            'link': '#'
        },
        {
            'id': 2,
            'title': 'Cookies',
            'link': '#'
        },
        {
            'id': 3,
            'title': 'Help',
            'link': '#'
        },
        {
            'id': 4,
            'title': 'FQAs',
            'link': '#'
        }
    ]
    
</script>
<template>
    <!-- Footer Start -->
    <div class="container-fluid bg-primary text-light footer wow fadeIn" data-wow-delay="0.1s">
        <div class="container py-5 px-lg-5">
            <div class="row g-5">
                <div class="col-md-6 col-lg-3">
                    <h4 class="text-white mb-4">{{ wiget1 }}</h4>
                    <p v-for="info in infoWidgets" :key="info.id"><i class="me-3" :class="info.icon">{{ info.title }}</i></p>
                    <div class="d-flex pt-2">
                        <a v-for="social in socials" :key="social.id" class="btn btn-outline-light btn-social" :href="social.link"><i :class="social.icon"></i></a>
                    </div>
                </div>
                <div class="col-md-6 col-lg-3">
                    <h4 class="text-white mb-4">{{ wiget2 }}</h4>
                    <a v-for="menu in menuItems" :key="menu.id" class="btn btn-link" :href="menu.link">{{ menu.title }}</a>
                </div>
                <div class="col-md-6 col-lg-3">
                    <h4 class="text-white mb-4">{{ wiget3 }}</h4>
                    <a v-for="menu in menuItems" :key="menu.id" class="btn btn-link" :href="menu.link">{{ menu.title }}</a>
                </div>
                <div class="col-md-6 col-lg-3">
                    <h4 class="text-white mb-4">{{ wiget3 }}</h4>
                    <p>{{ content }}</p>
                    <div class="position-relative w-100 mt-3">
                        <input class="form-control border-0 rounded-pill w-100 ps-4 pe-5" type="text" placeholder="Your Email" style="height: 48px;">
                        <button type="button" class="btn shadow-none position-absolute top-0 end-0 mt-1 me-2"><i class="fa fa-paper-plane text-primary-gradient fs-4"></i></button>
                    </div>
                </div>
            </div>
        </div>
        <div class="container px-lg-5">
            <div class="copyright">
                <div class="row">
                    <div class="col-md-6 text-center text-md-start mb-3 mb-md-0">
                        &copy; {{ text }} <a class="border-bottom" :href="link">{{ name }}</a>
                    </div>
                    <div class="col-md-6 text-center text-md-end">
                        <div class="footer-menu">
                            <a v-for="menu2 in menuItems2" :key="menu2.id" :href="menu2.link">{{ menu2.title }}</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Footer End -->


    <!-- Back to Top -->
    <a href="#" class="btn btn-lg btn-lg-square back-to-top pt-2"><i class="bi bi-arrow-up text-white"></i></a>
</template>
<style></style>