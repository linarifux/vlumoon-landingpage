<template>
    <div class="features-container">
        <section class="features" id="features">
            <div class="title">
                <h1>Product Features</h1>
                <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Officiis labore quasi autem qui repudiandae nulla!</p>
            </div>
            <div class="feature-items">
                <Icon v-for="(item, index) in iconList" :key="index" :data="item" />
            </div>
        </section>
    </div>
</template>

<script>
import Icon from './Icon.vue'
export default {
    props: ['iconList'],
    mounted() {
        console.log(this.mylist);
    },
    components: {
        Icon,
    }

}
</script>

<style>
.features-container{
    max-width: 60vw;
    margin: 0 auto;
}
.features {
    margin: 2rem auto;
    padding: 2rem 0;
}

.title {
    margin: 3rem auto;
    text-align: center;
}

.title h1 {
    font-size: 50px;
}

.title h1,
.title p {
    margin: 1rem 0;
}

.feature-items {
    margin: 5rem 0;
}

.feature-items {
    display: flex;
}

.feature-items {
    text-align: center;
}

@media screen and (max-width: 768px) {
.features-container{
    max-width: 90vw;
    margin: 0 auto;
}
.features {
    margin-top: 5rem;
    padding: 5rem 0;
}

.title {
    margin: 1rem;
    text-align: center;
}

.title h1 {
    font-size: 30px;
}

.title h1,
.title p {
    margin: 1rem 0;
}

.feature-items {
    margin: 2rem 0;
    display: block;
}

}
</style>