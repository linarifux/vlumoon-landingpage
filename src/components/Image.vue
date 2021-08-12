<template>
    <img class="jump" src="https://i.postimg.cc/MH0TnxNv/no-background.png" alt="VluMoon">
</template>

<script>
export default {

}
</script>

<style>
.jump {
    animation: jump 3s infinite;
}

@keyframes jump {
    50% {
        transform: translateY(50px)
    }
}
</style>