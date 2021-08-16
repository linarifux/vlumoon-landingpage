<template >
  <div class="carousel">
      <slot></slot>
      <button @click="prev" class="prev"><fa icon="chevron-left" /></button>
      <button @click="next" class="next"><fa icon="chevron-right"/></button>
  </div>
</template>

<script>
export default {
    methods: {
        next(){
            this.$emit("next")
        },
        prev(){
            this.$emit("prev")
        }
    },
}
</script>

<style>
    .carousel-slide{
        width: 100%;
        margin: 0 auto;
        position: relative;
    }
    .prev{
        position: absolute;
        left: 0%;
        top: 50%;
        transform: translateY(-50%);
    }
    .next{
        position: absolute;
        right: 0%;
        top: 50%;
        transform: translateY(-50%);
    }
</style>