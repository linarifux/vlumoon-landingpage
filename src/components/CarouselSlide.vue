<template>
    <div class="my-slide">
        <transition :name="direction" mode="">
            <div v-if="visibleSlide === index" class="carousel-slide">
                <slot></slot>
            </div>
        </transition>
    </div>
</template>

<script>
export default {
    props: ['visibleSlide', 'index', 'direction']
}
</script>

<style>
.my-slide{
    max-width: 40vw;
    text-align: center;
    background: #faf6f4;
    margin: 0 auto;
    border: none;
    border-radius: 10px;
    height: 120px;
}
.carousel-slide {
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


</style>