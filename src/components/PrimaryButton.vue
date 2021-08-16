<template>
    <button>{{buttonName}}</button>
</template>

<script>
export default {
    props: ['buttonName']
}
</script>

<style>
button {
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

@media screen and (max-width: 768px) {
  button{
    padding: 1rem 1rem;
    font-size: 18px;
  }
}
</style>