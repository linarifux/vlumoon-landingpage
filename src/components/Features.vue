<template>
    <div class="container">
        <section class="features" id="features">
            <div class="title">
                <h1>Product Features</h1>
                <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Officiis labore quasi autem qui repudiandae nulla!</p>
            </div>
            <div class="feature-items">
                <Icon v-for="(item, index) in iconList" :key="index" :data="item"/>
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
.features {
    margin: 5rem auto;
    padding: 5rem 0;
}

.title {
    width: 50%;
    margin: 3rem auto;
    text-align: center;
}
.title h1{
    font-size: 30px;
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
    margin: 0 1rem;
}
</style>