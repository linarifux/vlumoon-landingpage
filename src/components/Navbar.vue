<template>
    <div class="nav-menu">
        <div class="logo-area">
            <a href="#">Logo</a>
        </div>
        <div class="menu-area">
            <ul>
                <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="/">Home</a></li>
                <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="#features">Features</a></li>
                <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="#about">About</a></li>
                <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="#product">Product</a></li>
                <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="#testimonial">Testimonial</a></li>
                <li @click="clickHandler" v-bind:class="{active: isActive}"><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
        }
    },
    methods: {
        clickHandler(){
        }
    },
}
</script>

<style>
.active{
    border-bottom: 1px solid black;
}
.nav-menu {
    position: fixed;
    display: flex;
    align-items: center;
    gap: 30rem;
    top: 0;
    padding: 2rem 0;
    background: #FFEBE2;
    width: 100%;
    z-index: 10000;
}

.logo-area {
    font-size: 20px;
    margin-left: 20vw
}

.menu-area ul {
    display: flex;
}

.menu-area>ul>li a {
    margin: 0 .5rem;
    font-size: 18px;
    padding: .5rem .5rem;
}
</style>