<template>
    <div class="my-nav">
        <Navbar />
    </div>
    <div class="my-honme">
        <Home />
    </div>
    <div class="container">
        <Features :iconList="myList" />
        <About />
        <Choose :iconList="myList" />
        <Products :products="products" />
    </div>
    <Newsletter />
    <div class="container">
        <Testimonial />
    </div>
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
    },
    data() {
        return {
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

a {
    text-decoration: none;
    color: #000;
}

li {
    list-style: none;
}

.container {
    max-width: 60vw;
    margin: 2rem auto;
}

.my-honme{
    background-image: url('https://i.postimg.cc/2yr6CdsW/banner-1.png');
    background-size: cover;
}
</style>
