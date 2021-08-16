<template>
    <div class="newsletter-wrapper">
        <div class="newsletter-container">
            <div class="newsletter">
                <div class="title">
                    <h1>Subscribe Our Newsletter</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi odio at, eius reiciendis recusandae quos.</p>
                </div>
                <div class="form-control">
                    <form action="#">
                        <div class="input-field">
                            <input type="email" placeholder="Enter Your Email">
                            <div class="subscribe-button">
                                <PrimaryButton :buttonName="buttonName" />
                            </div>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import PrimaryButton from './PrimaryButton.vue'
export default {
    components: {
        PrimaryButton,
    },
    data() {
        return {
            buttonName: "Subscribe"
        }
    },
}
</script>

<style scoped>
.newsletter-container {
    max-width: 60vw;
    margin: 0 auto;
    align-items: center;
}

.newsletter-wrapper {
    background-image: url('https://i.postimg.cc/QtC31tQz/banner-3.jpg');
    background-size: cover;
    padding: 5rem 0;
    margin: 2rem 0;
}

.newsletter .title {
    color: #fff;
}

.newsletter .title h1 {
    line-height: 0;
    margin-bottom: 2rem;
}

.newsletter .title p {
    margin: 0 auto;
}

form{
    width: 80%;
    padding: 5rem;
    background: #fff;
    border-radius: 25px;
    margin: 0 auto;
}

.input-field {
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    border: 1px solid gray;
    border-radius: 50px;
}

input {
    border: none;
    outline: none;
    font-size: 18px;
    margin: 0 2rem;
    width: 100%;
}

button {
    border-radius: 50px;
}

button:hover {
    background: #b83a17;
}

@media screen and (max-width: 768px) {
    .newsletter-container {
        max-width: 90vw;
    }
    .newsletter-wrapper {
        padding: 2rem 0;
    }
    .newsletter .title h1 {
        line-height: inherit;
        font-size: 30px;
    }
    form{
    width: 100%;
    padding: 1rem;
    margin: 0 auto;
}
    .input-field {
        display: block;
        border: none;
        border-radius: 50px;
    }
    input[type="email"] {
        border: 1px solid black;
        border-radius: 10px;
        outline: none;
        font-size: 15px;
        margin: 0;
        padding: 1rem .5rem;
        width: 100%;
    }
    .subscribe-button{
        margin: 10px 0;
        text-align: center;
    }
    button {
        border-radius: 10px;
        padding: 1rem 1rem;
        font-size: 15px;
    }
}
</style>