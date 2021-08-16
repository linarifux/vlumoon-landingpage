<template>
    <div class="home-container">
        <section class="home-page" id="home">
            <div class="home-text">
                <h1>Leather Pan Handle Cover for Cast Iron Skillets</h1>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quae placeat eaque saepe repudiandae quia voluptates.</p>
                <div class="primary-btn">
                    <PrimaryButton :buttonName="buttonName" />
                </div>
            </div>
            <div class="image-area">
                <Image />
            </div>
        </section>
    </div>
</template>

<script>
import Image from './Image.vue'
import PrimaryButton from './PrimaryButton.vue'
// @ is an alias to /src

export default {
    data() {
        return {
            buttonName: 'Buy Products'
        }
    },
    name: 'Home',
    components: {
        Image,
        PrimaryButton,
    }
}
</script>

<style scoped>
.home-container {
    background-image: url('https://i.postimg.cc/2yr6CdsW/banner-1.png');
    background-size: cover;
}

.home-page img {
    height: 300px;
}

.home-page {
    max-width: 60vw;
    margin: 0rem auto;
    display: flex;
    justify-content: space-between;
    padding: 5rem 0;
    align-items: center;
}

.home-text h1 {
    font-size: 50px;
    font-weight: 700;
    padding: 1rem 0;
    letter-spacing: 3px;
    max-width: 90%;
}

.home-text p {
    font-size: 20px;
    letter-spacing: 1px;
    line-height: 2rem;
    padding: 1rem 0;
    max-width: 75%;
}

.primary-btn {
    padding: 2rem 0;
}

.primary-btn button {
    padding: 1.2rem 3rem;
    font-size: 20px;
    font-weight: 700;
    cursor: pointer;
    border: none;
    border-radius: 5px;
    background: #FF4D1C;
    color: #fff;
    transition: all .5s;
}

.primary-btn button:hover {
    background: #c73912;
}

@media screen and (max-width: 768px) {
    .home-page img {
        height: 200px;
    }
    
    .home-page {
        max-width: 90vw;
        display: block;
        padding: 2rem 0;
        text-align: center;
    }
    .home-text h1 {
        font-size: 30px;
        font-weight: 700;
        padding: 1rem .5rem;
        letter-spacing: 2px;
        max-width: 100%;
    }
    .home-text p {
        font-size: 20px;
        letter-spacing: 1px;
        line-height: 2rem;
        padding: 1rem 0;
        max-width: 100%;
    }
    .primary-btn {
        padding: 1rem 0;
    }
    .primary-btn button {
        padding: 1rem 1.5rem;
        font-size: 16px;
        font-weight: 700;
    }
}
</style>
