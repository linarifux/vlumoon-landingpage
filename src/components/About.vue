<template>
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
.about .image-area img {
    height: 300px;
}

.about {
    display: flex;
    gap: 5rem;
    padding: 8rem 0;
    margin: 2rem 0;
}

.about .image-area {
    width: 50%;
    text-align: right;
    padding: 0 2rem;
}

.about .text-area {
    background: #fff;
    width: 50%;
    border-radius: 5px;
    padding: 1rem 2rem;
    box-shadow: 0px 0px 15px;
}

.about-title h1 {
    margin: 1rem 0;
}

.about-title p {
    font-size: 14px;
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
</style>