<template>
    <div class="testimonial-container">
        <section class="testimonial-area" id="testimonial">
            <div class="title">
                <h1>Our Customer Feedback</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Est exercitationem amet nisi possimus repellendus recusandae!</p>
            </div>
            <div class="customers">
                <Carousel @next="next" @prev="prev">
                    <CarouselSlide v-for="(item,index) in customers" :key="index" :index="index" :visibleSlide="visibleSlide" :direction="direction">
                        <img :src="item.image" :alt="item.name">
                        <h3>{{item.name}}</h3>
                        <p class="job">{{item.job}}</p>
                        <fa icon="quote-left" class="quote" />
                        <fa v-for="(item,index) in 5" :key="index" icon="star" class="star" />
                        <p class="feedback">{{item.feedback}}</p>
                    </CarouselSlide>
                </Carousel>
            </div>
        </section>
    </div>
</template>

<script>
import Carousel from './Carousel.vue'
import CarouselSlide from './CarouselSlide.vue'

export default {
    components: {
        Carousel,
        CarouselSlide,
    },
    data() {
        return {
            direction: 'left',
            customers: [
                { id: 1, name: 'Andrew Watt', image: 'https://picsum.photos/200', job: 'Graphic Designer', feedback: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero, quisquam ad? Consectetur sequi illum placeat ratione voluptates ad, quasi et' },
                { id: 2, name: 'John Smith', image: 'https://picsum.photos/200', job: 'Web Developer', feedback: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero, quisquam ad? Consectetur sequi illum placeat ratione voluptates ad, quasi et' },
                { id: 3, name: 'Anna Perry', image: 'https://picsum.photos/200', job: 'Software Designer', feedback: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero, quisquam ad? Consectetur sequi illum placeat ratione voluptates ad, quasi et' },
                { id: 4, name: 'Mosh Hammadani', image: 'https://picsum.photos/200', job: 'SQA Engineer', feedback: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero, quisquam ad? Consectetur sequi illum placeat ratione voluptates ad, quasi et' },
            ],
            visibleSlide: 0,
        }
    },
    computed: {
        customersLength() {
            return this.customers.length
        }
    },
    methods: {
        next() {
            if (this.visibleSlide >= this.customersLength - 1) {
                this.visibleSlide = 0
            } else {
                this.visibleSlide++
            }
            this.direction = 'left'
            console.log(this.direction);
        },
        prev() {
            if (this.visibleSlide === 0) {
                this.visibleSlide = this.customersLength - 1
            } else {
                this.visibleSlide--
            }
            this.direction = 'right'
        }
    },

}
</script>

<style>
.testimonial-container {
    max-width: 60vw;
    margin: 0 auto;
}

.testimonial-area {
    margin: 2rem 0;
    padding: 2rem 0;
}
.customers {
    max-width: 40vw;
    text-align: center;
    background: #faf6f4;
    margin: 0 auto;
    border: none;
    border-radius: 10px;
    height: 500px;
    position: relative;
}

.my-slide {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}

.left-enter-active {
    animation: leftInAnimation .4s ease-in-out;
}

.left-leave-active {
    animation: leftOutAnimation .4s ease-in-out;
}

.right-enter-active {
    animation: rightInAnimation .4s ease-in-out;
}

.right-leave-active {
    animation: rightOutAnimation .4s ease-in-out;
}

.customers .feedback {
    max-width: 50%;
    margin: .5rem auto;
    font-size: 15px;
    letter-spacing: 1px;
}

.customers img {
    border: none;
    border-radius: 100px;
    margin: 1rem 0;
}

.customers h3 {
    letter-spacing: 2px;
    margin: .5rem 0;
    font-size: 25px;
}

.customers .job {
    letter-spacing: 2px;
    font-size: 18px;
    margin: .5rem 0;
}

.customers .quote {
    display: block;
    margin: .5rem auto;
    font-size: 35px;
}

.customers .star {
    color: goldenrod;
    margin: .5rem 0;
}

@keyframes leftInAnimation {
    from {
        transform: translateX(100%);
    }
    to {
        transform: translateX(0%);
    }
}

@keyframes leftOutAnimation {
    from {
        transform: translateX(0);
    }
    to {
        transform: translateX(-100%);
    }
}

@keyframes rightInAnimation {
    from {
        transform: translateX(-100%);
    }
    to {
        transform: translateX(0%);
    }
}

@keyframes rightOutAnimation {
    from {
        transform: translateX(0);
    }
    to {
        transform: translateX(100%);
    }
}

/* Mobile view */

@media screen and (max-width: 768px) {
    .testimonial-container{
        max-width: 90vw;
    }
    .testimonial-area .title{
        max-width: 100%;
        text-align: center;
    }
    .customers {
        max-width: 100%;
    }
    .my-slide {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
    }
    .left-enter-active {
        animation: leftInAnimation .4s ease-in-out;
    }
    .left-leave-active {
        animation: leftOutAnimation .4s ease-in-out;
    }
    .right-enter-active {
        animation: rightInAnimation .4s ease-in-out;
    }
    .right-leave-active {
        animation: rightOutAnimation .4s ease-in-out;
    }
    .my-slide .feedback {
        max-width: 50%;
        margin: .5rem auto;
        font-size: 15px;
        letter-spacing: 1px;
    }
    .my-slide img {
        border: none;
        border-radius: 100px;
        margin: 1rem 0;
    }
    .my-slide h3 {
        letter-spacing: 2px;
        margin: .5rem 0;
        font-size: 20px;
    }
    .my-slide .job {
        letter-spacing: 2px;
        font-size: 15px;
        margin: .5rem 0;
    }
    .my-slide .quote {
        display: block;
        margin: .5rem auto;
        font-size: 25px;
    }
    .my-slide .star {
        color: goldenrod;
        margin: .5rem 0;
    }
}



.customers .feedback {
    max-width: 100%;
    margin: .5rem auto;
    font-size: 18px;
    letter-spacing: 1px;
}

.customers img {
    border: none;
    border-radius: 100px;
    margin: 1rem 0;
}
</style>