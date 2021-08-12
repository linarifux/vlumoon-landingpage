<template>
    <div class="choose-area">
        <div class="choose-title">
            <h1>Why Choose The Product</h1>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Consequatur doloribus atque totam, distinctio autem quisquam cumque itaque! Laboriosam, dolores ducimus?</p>
        </div>
        <div class="choose-content">
            <div class="slide-area">
                <img :src="images[imageSrc]" alt="VluMoon">
                <div class="button-area">
                    <button @click="backwardImageIndex"><fa icon="chevron-left" /></button><button @click="forwardImageIndex"><fa icon="chevron-right" /></button>
                </div>
            </div>
            <div class="spec-area">
                <Icon v-for="(item, index) in iconList" :key="index" :data="item"/>
            </div>
        </div>
    </div>
</template>

<script>
import Icon from './Icon.vue'
export default {
    data() {
        return {
            images: ['https://i.postimg.cc/fW6fgk3x/Untitled-design-29.png','https://i.postimg.cc/MH0TnxNv/no-background.png'],
            imageSrc : 0,
        }
    },
    methods: {
        forwardImageIndex(){
            if(this.imageSrc >= this.images.length-1){
                this.imageSrc = 0
            }else{
                this.imageSrc ++
            }
        },
        backwardImageIndex(){
            if(this.imageSrc <= 0){
                this.imageSrc = this.images.length - 1
            }else{
                this.imageSrc --
            }
        }
    },
    props: ['iconList'],
    components: {
        Icon,
    }

}
</script>

<style>
.choose-area {
    margin: 8rem 0;
}
.choose-title{
    text-align: center;
    margin: 3rem 0;
}
.choose-title h1, .choose-title p{
    margin: 1rem 0;
}
.choose-title p{
    width: 50%;
    margin: 0 auto;
}
.choose-area img{
    height: 300px;
    transition: .5s ease-in-out;
}
.choose-content{
    display: flex;
    gap: 6rem;
    align-items: center;
}
.slide-area{
    background: #fff;
    text-align: center;
    padding: 1rem 5rem;
    height: 400px;
    box-shadow: 0px 0px 20px;
    border-radius: 5px;
}
.spec-area{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    text-align: center;
}

.button-area{
    padding: 1.5rem 0;
}
.button-area button{
    padding: .5rem 1rem;
    margin: 0 1rem;
    border: none;
    background: #000;
    color: #fff;
    cursor: pointer;
    border-radius: 5px;
}
</style>