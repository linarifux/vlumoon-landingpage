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
</style>