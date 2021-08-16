<template>
    <div class="products-container">
        <section class="products-area" id="product">
            <div class="title">
                <h1>Our Awesome Products</h1>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Distinctio, quam placeat perferendis in reiciendis veritatis.</p>
            </div>
            <div class="all-products">
                <div class="single-product">
                    <Product v-for="(item, index) in products" :key="index" :product="item" />
                </div>
                <div class="primary-btn">
                    <PrimaryButton :buttonName="buttonName" />
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import PrimaryButton from './PrimaryButton.vue'
import Product from './Product.vue'
export default {
    props: ['products'],
    components: {
        PrimaryButton,
        Product,
    },
    data() {
        return {
            buttonName: 'More Products'
        }
    },
}
</script>

<style scoped>
.products-container{
    max-width: 60vw;
    margin: 0 auto;
}
.products-area {
    margin: 2rem 0;
    padding: 2rem 0;
}

.single-product {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
}

.primary-btn {
    text-align: center;
    margin: 5rem 0;
}

.primary-btn button:hover {
    background: #d84015;
}

@media screen and (max-width: 768px) {
.products-container{
    max-width: 90vw;
    margin: 0 auto;
}
.single-product {
    display: block;
}

.primary-btn {
    text-align: center;
    margin: 2rem 0;
}
}
</style>