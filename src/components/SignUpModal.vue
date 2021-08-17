<template>
    <div class="my-modal">
        <div class="modal-close" @click="closeModal">
            <fa icon="times" class="times-icon" />
        </div>
        <div class="modal-container">
            <div class="image-area">
                <img src="https://i.postimg.cc/MH0TnxNv/no-background.png" alt="VluMoon">
            </div>
            <div class="sign-up">
                <h1>Sign Up To Win</h1>
                <p>Enter and receive launch specials & our discount offers.</p>
            </div>
            <div class="singup-input-fields">
                <h4>You'll also be informed of new releases, receive exclusive offers and view behind-the-scenes coverage.</h4>
                <input type="email" placeholder="Email">
                <PrimaryButton :buttonName="buttonName" />
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
            buttonName: 'Sign Up'
        }
    },
    methods: {
        closeModal() {
            this.$emit('closeModal')
        }
    },
}
</script>

<style>
.my-modal {
    position: absolute;
    top: 1vw;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: 99999;
    height: 100%;
    max-width: 50vw;
    margin: 0 auto;
    background: rgb(207, 202, 202);
    opacity: .95;
    border-radius: 10px;
}

.modal-close {
    position: absolute;
    right: .5vw;
    top: .5vw;
    background: #000;
    color: #fff;
    font-size: 20px;
    padding: .5rem 1rem;
    border-radius: 5px;
    cursor: pointer;
}

.modal-container {
    max-width: 40vw;
    margin: 2rem auto;
}

.sign-up {
    background: #000;
    color: #fff;
    text-align: center;
    border-radius: 5px;
    padding: 1rem 0;
    margin: 2rem 0;
}

.sign-up h1 {
    margin: 1rem 0;
    letter-spacing: 2px;
}

p {
    letter-spacing: 1px;
}

.singup-input-fields {
    text-align: center;
    margin: 3rem 0;
}

.singup-input-fields input {
    display: block;
    width: 100%;
    padding: .5rem 1rem;
    background: none;
    border: none;
    border: 1px solid #fff;
    border-radius: 5px;
    font-size: 20px;
    margin: 1rem 0;
    outline: none;
}

.singup-input-fields h4 {
    font-size: 18px;
}

.singup-input-fields button {
    padding: .8rem 2rem;
    font-size: 20px;
    width: 100%
}

.singup-input-fields button:hover{
    background: #ce3f18;
}

.image-area {
    text-align: center;
}

img {
    height: 300px;
}

@media screen and (max-width: 768px) {
    .my-modal {
        max-width: 90vw;
    }
    .modal-close {
        right: 1vw;
        top: 1vw;
        font-size: 18px;
        padding: .2rem .5rem;
    }
    .modal-container {
        max-width: 80vw;
        margin: 1rem auto;
    }
    .sign-up {
        padding: 1rem 0;
        margin: 1rem 0;
    }
    .singup-input-fields {
        margin: 2rem 0;
    }
    .singup-input-fields input {
        margin: 1rem 0;
    }
    .singup-input-fields h4 {
        font-size: 18px;
    }
    
}
</style>