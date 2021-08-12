<template>
  <div class="container">
    <section class="home-page" id="home">
      <div class="text-area">
        <h1>Leather Pan Handle Cover for Cast Iron Skillets</h1>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quae placeat eaque saepe repudiandae quia voluptates.</p>
        <div class="primary-btn">
          <PrimaryButton :buttonName="buttonName"/>
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
  .home-page img{
    height: 300px;
  }
  .home-page{
    padding: 5rem 0;
    display: flex;
  }
  .home-page .text-area, .home-page .image-area{
    width: 50%;
  }
  .home-page .image-area{
    text-align: right;
    padding: 5rem 0;
  }

  .home-page .text-area h1{
    font-size: 50px;
    letter-spacing: 2px;
    padding: 2rem 0;
    font-weight: 700;
  }

  .home-page .text-area p{
    font-size: 20px;
    letter-spacing: 1px;
    line-height: 2rem;
    padding: 2rem 0;
  }

  .primary-btn button{
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

  .primary-btn button:hover{
    background: #c73912;
  }

</style>
