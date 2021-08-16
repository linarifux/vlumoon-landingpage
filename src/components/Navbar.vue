<template>
    <div class="nav-items">
        <div class="logo">
            <p>LOGO</p>
        </div>
        <div class="mobile-menu" @click="toggleMenu">
            <fa icon="bars" class="bars-icon" v-if="!isMenuActive"/>
            <fa icon="times" class="times-icon" v-if="isMenuActive" />
        </div>
        <ul v-bind:class="{active: isMenuActive}">
            <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="/">Home</a></li>
            <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="#features">Features</a></li>
            <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="#about">About</a></li>
            <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="#product">Product</a></li>
            <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="#testimonial">Testimonial</a></li>
            <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="#contact">Contact</a></li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isMobileView: true,
            isMenuActive: false
        }
    },
    methods: {
        toggleMenu(){
            this.isMenuActive = !this.isMenuActive
        }
    },

}
</script>

<style scoped>
.nav-items{
    width: 80vw;
    display: flex;
    margin: 0 auto;
    justify-content: space-between;
    align-items: center;
}
.logo{
    font-size: 20px;
}
ul {
    list-style: none;
    display: flex;
}

ul>li {
    margin: 0 1rem;
}

a {
    padding: .5rem 0;
    align-items: center;
    display: flex;
    font-size: 20px;
    text-decoration: none;
    color: #000;
    margin: 0 1rem;
}
.bars-icon{
    display: none;
}

@media screen and (max-width: 768px) {
    .nav-items{
        width: 90vw;
    }
    .bars-icon{
        display: block;
        transition: .5s;
    }
    ul{
        display: none;
        transition: .5s ease-in-out;
    }
    .active{
        position: absolute;
        left: 0;
        top: 5rem;
        display: block;
        width: 100%;
        background: #fff;
        transition: .5s ease-in-out;
    }
    .active li{
        background: #000000;
        width: 100%;
        color: #fff;
        transition: .5s;
        margin: 0 auto;
        border-bottom: 1px solid #fff;
    }   
    a{
        color: #fff;
    }
    .mobile-menu{
        font-size: 20px;
    }
}
</style>