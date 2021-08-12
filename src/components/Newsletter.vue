<template>
    <div class="newsletter">
        <div class="container">
            <div class="title">
                <h1>Subscribe Our Newsletter</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi odio at, eius reiciendis recusandae quos.</p>
            </div>
            <div class="form-control">
                <form action="#">
                    <div class="input-field">
                        <input type="email" placeholder="Enter Your Email">
                        <div class="subscribe-button">
                            <button>Subscribe</button>
                        </div>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.newsletter {
    background-image: url('https://i.postimg.cc/QtC31tQz/banner-3.jpg');
    background-size: cover;
    padding: 5rem 0;
    margin: 5rem 0;
}

.newsletter .title {
    color: #fff;
}

.newsletter .title p {
    margin: 0 auto;
}
.form-control{
    width: 70%;
    padding: 5rem;
    background: #fff;
    border-radius: 25px;
    margin: 0 auto;
}
.input-field{
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    border: 1px solid gray;
    border-radius: 50px;
}
input{
    border: none;
    outline: none;
    font-size: 18px;
    margin: 0 2rem;
    width: 100%;
}
button{
    border-radius: 50px;
}
button:hover{
    background: #b83a17;
}
</style>