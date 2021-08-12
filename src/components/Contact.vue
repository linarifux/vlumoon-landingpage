<template>
    <section class="contact-page" id="contact">
        <div class="contact-area">
            <div class="contact-title">
                <h1>Contact With Us</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius, iusto! Maxime expedita eos labore cum.</p>
            </div>
            <div class="contact-content">
                <div class="contact-form">
                    <form action="#">
                        <input type="text" placeholder="Name*" class="contact-name">
                        <input type="email" placeholder="Email*" class="contact-email">
                        <textarea name="message" id="message" class="contact-message" placeholder="Write Your Message*"></textarea>
                        <div class="primary-btn"><button>Submit</button></div>
                    </form>
                </div>
                <div class="contact-image">
                    <Image />
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import Image from './Image.vue'
export default {
    components: {
        Image,
    }
}
</script>

<style>
.contact-page{
    background: #FAF6F4;
    padding: 4rem 0;

}
.contact-area {
    max-width: 60vw;
    margin: 0 auto;
    padding: 0;
}

.contact-title {
    margin: 5rem 0;
}

.contact-title h1 {
    margin: .5rem 0;
}

.contact-title p {
    width: 60%;
}

.contact-content {
    display: flex;
    gap: 10rem;
}

.contact-form input {
    display: block;
    width: 40rem;
    padding: .5rem 1rem;
    margin: 1rem 0;
    border: none;
    border-bottom: 1px solid rgb(184, 177, 177);
    font-size: 18px;
    outline: none;
    background: none;
}
.contact-form textarea{
    width: 40rem;
    height: 10rem;
    padding: .5rem 1rem;
    margin: 1rem 0;
    border: none;
    border-bottom: 1px solid rgb(184, 177, 177);
    font-size: 18px;
    outline: none;
    background: none;
}
.contact-image{
    display: block;
    align-items: center;
}

.contact-image img {
    height: 300px;
}

.contact-form .primary-btn button:hover{
    background: #d13c12;
}
</style>