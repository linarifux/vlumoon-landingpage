<template>
    <div class="about-container">
        <section class="about" id="about">
            <div class="image-area">
                <Image />
            </div>
            <div class="text-area">
                <div class="about-title">
                    <h1>About The Product</h1>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa, aliquam.</p>
                </div>
                <div class="list">
                    <ul>
                        <li>
                            <fa icon="check" class="check" /> Model No #240 Blackmart</li>
                        <li>
                            <fa icon="check" class="check" /> Model No #240 Blackmart</li>
                        <li>
                            <fa icon="check" class="check" /> Model No #240 Blackmart</li>
                        <li>
                            <fa icon="check" class="check" /> Model No #240 Blackmart</li>
                        <li>
                            <fa icon="check" class="check" /> Model No #240 Blackmart</li>
                        <li>
                            <fa icon="check" class="check" /> Model No #240 Blackmart</li>
                        <li>
                            <fa icon="check" class="check" /> Model No #240 Blackmart</li>
                    </ul>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import Image from './Image.vue'
export default {
    components: {
        Image,
    }

}
</script>

<style scoped>
.about-container {
    max-width: 60vw;
    margin: 0 auto;
}

.about .image-area img {
    height: 300px;
}

.about {
    display: flex;
    justify-content: space-around;
    padding: 6rem 0;
    margin: 2rem 0;
}

.about .text-area {
    background: #fff;
    border-radius: 5px;
    padding: 2rem 2rem;
    box-shadow: 0px 0px 15px;
}

.about-title h1 {
    margin: 1rem 0;
    font-size: 40px;
    line-height: 0;
}

.about-title p {
    font-size: 16px;
    margin: 2rem 0;
}

.list {
    margin-top: 2rem;
}

.list>ul>li {
    font-size: 15px;
    line-height: 2rem;
}

.list .check {
    color: green;
    margin-right: 5px;
}

@media screen and (max-width: 768px) {
    .about-container {
        max-width: 90vw;
        margin: 0 auto;
    }
    .about .image-area{
        text-align: center;
        padding-bottom: 5rem;
    }
    .about .image-area img {
        height: 200px;
    }
    .about {
        display: block;
        padding: 5rem 0;
    }
    .about-title h1 {
        font-size: 30px;
    }
 
}
</style>