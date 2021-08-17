<template>
<SignUpModal v-if="showModal" @closeModal="closeModal"/>
<div class="nav-bar">
    <Navbar />
</div>
    <Home />
    <Features :iconList="myList" />
    <About />
    <Choose :iconList="myList" />
    <Products :products="products" />
    <Newsletter />
    <Testimonial />
    <Contact />
    <Footer />
</template>

<script>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import Features from './components/Features.vue'
import About from './components/About.vue'
import Choose from './components/Choose.vue'
import Products from './components/Products.vue'
import Newsletter from './components/Newsletter.vue'
import Testimonial from './components/Testimonial.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
import SignUpModal from './components/SignUpModal.vue'

export default {
    name: 'App',
    components: {
        Navbar,
        Home,
        Features,
        About,
        Choose,
        Products,
        Newsletter,
        Testimonial,
        Contact,
        Footer,
        SignUpModal
    },
    mounted() {
        setTimeout(()=>{
            this.showModal = true
        },5000)
    },
    methods: {
        closeModal(){
            this.showModal = false
        }
    },
    data() {
        return {
            showModal: false,
            myList: [{
                    id: 1,
                    icon: 'wrench',
                    title: 'High Quality',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, iusto!'
                },
                {
                    id: 2,
                    icon: 'wrench',
                    title: 'High Quality',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, iusto!'
                },
                {
                    id: 3,
                    icon: 'wrench',
                    title: 'High Quality',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, iusto!'
                },
                {
                    id: 4,
                    icon: 'wrench',
                    title: 'High Quality',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, iusto!'
                },
            ],
            products: [
                { id: 1, image: 'https://i.postimg.cc/fW6fgk3x/Untitled-design-29.png', title: 'Leather Cast Iron Handle', price: 10, oldPrice: 15, features: ['High Quality', 'Heat Resistant up to 450 Degrees', 'Fit nicely'] },
                { id: 2, image: 'https://i.postimg.cc/fW6fgk3x/Untitled-design-29.png', title: 'Leather Cast Iron Handle', price: 12, oldPrice: 16, features: ['High Quality', 'Heat Resistant up to 450 Degrees', 'Fit nicely'] },
                { id: 3, image: 'https://i.postimg.cc/fW6fgk3x/Untitled-design-29.png', title: 'Leather Cast Iron Handle', price: 10, oldPrice: 15, features: ['High Quality', 'Heat Resistant up to 450 Degrees', 'Fit nicely'] },
                { id: 4, image: 'https://i.postimg.cc/fW6fgk3x/Untitled-design-29.png', title: 'Leather Cast Iron Handle', price: 12, oldPrice: 16, features: ['High Quality', 'Heat Resistant up to 450 Degrees', 'Fit nicely'] },
            ]
        }
    },
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: #FFEBE2;
}

.nav-bar{
    position: fixed;
    background: #FFEBE2;
    width: 100%;
    height: 80px;
    z-index: 999;
    align-items: center;
    display: flex;
}
</style>
