<script setup>
    import Header from './components/Header.vue'
    import About from './components/About.vue'
    import Feature from './components/Feature.vue'
    import Screenshot from './components/Screenshot.vue'
    import Process from './components/Process.vue'
    import Download from './components/Download.vue'
    import Pricing from './components/Pricing.vue'
    import Testimonial from './components/Testimonial.vue'
    import Contact from './components/Contact.vue'
    import Footer from './components/Footer.vue'

</script>

<template>
    <div class="container-xxl bg-white p-0">
        <!-- Spinner Start -->
        <div id="spinner" class="show bg-white position-fixed translate-middle w-100 vh-100 top-50 start-50 d-flex align-items-center justify-content-center">
            <div class="spinner-grow text-primary" style="width: 3rem; height: 3rem;" role="status">
                <span class="sr-only">Loading...</span>
            </div>
        </div>
        <!-- Spinner End -->
        <Header/>
        <About/>
        <Feature/>
        <Screenshot/>
        <Process/>
        <Download/>
        <Pricing/>
        <Testimonial/>
        <Contact/>
        <Footer/>
        
    </div>
</template>

<style scoped>

</style>
