<template>
    <div class="product">
        <div class="product-image">
            <img :src="product.image" alt="">
        </div>
        <div class="product-details">
            <h3>{{product.title}}</h3>
            <div class="product-features">
                <ul>
                    <li v-for="(item,index) in product.features" :key="index">
                        <fa icon="check" class="check" /> {{item}}</li>
                </ul>
            </div>
            <div class="product-price">
                <p>${{product.price}}</p><span>${{product.oldPrice}}</span>
            </div>
            <div class="order-button">
                <button>Order Now</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['product']
}
</script>

<style>
.product-image img {
    height: 200px;
}

.product {
    display: flex;
    margin: 5px;
    background: #fff;
    border-radius: 5px;
    box-shadow: 0px 0px 5px 0px;
    padding: .5rem 1rem;
    gap: 2rem;
}

.order-button button {
    padding: .5rem 1rem;
    margin: 0;
    font-size: 15px;
    transition: .5s ease-in-out;
}

.order-button button:hover {
    background: #c73b14;
}

.product-details h3 {
    margin: .5rem 0;
}

.product-details li {
    font-size: 13px;
    margin: 5px;
}

.product-details .product-price {
    display: flex;
    gap: 2rem;
    margin: 1rem 0;
    position: relative;
    padding: .5rem 0;
}

.product-price span {
    text-decoration: line-through;
    position: absolute;
    left: 3rem;
    top: -.08rem;
}

.product-details .check {
    color: green;
}

@media screen and (max-width: 768px) {
    .product-image img{
        height: 150px;
    }
    .product {
        display: block;
        margin: 20px 0;
        padding: 1rem 1rem;
    }
    .product-image{
        text-align: center;
    }
    .order-button{
        text-align: center;
    }
    .product-details h3 {
        text-align: center;
    }
    .product-details ul{
        width: 80%;
        margin: 0 auto;
    }
    .product-details .product-price {
        padding: 1rem;
        width: 80%;
        margin: 0 auto;
    }
    .product-price span {
        padding: .5rem;
    }
}
</style>