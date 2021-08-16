<template>
    <div class="nav-items">
        <div class="logo">
            <p>LOGO</p>
        </div>
        <div class="mobile-menu" v-if="isMobileView" @click="toggleMenu">
            <fa icon="bars" class="bars-icon" />
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
    width: 60vw;
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
    .bars-icon{
        display: block;
    }
    ul{
        display: none;
    }
    .active{
        position: absolute;
        left: 0;
        top: 5rem;
        display: block;
        width: 100%;
        background: #fff;
    }
    .active li{
        background: #FFE4D8;
        width: 100%;
        margin-left: 0;
        margin: .5rem auto;
    
    }
}
</style>