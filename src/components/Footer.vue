<template>
    <div class="footer-container">
        <div class="footer-area">
            <div class="social-icons">
                <p>Follow Us: </p>
                <i class="fab fa-facebook-f"></i>
                <i class="fab fa-twitter"></i>
                <i class="fab fa-instagram"></i>
            </div>
            <div class="all-rights">
                <p>All Rights Reserved.</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.footer-container {
    background: #000;
}

.footer-area {
    display: flex;
    max-width: 60vw;
    margin: 0 auto;
    justify-content: space-between;
    padding: 1rem 0;
    align-items: center;
}

.social-icons {
    color: #fff;
    display: flex;
    align-items: center;
    gap: 2rem;
}

.social-icons i{
    padding: .5rem;
    border: 1px solid #fff;
    border-radius: 5px;
    text-align: center;
    cursor: pointer;
}

.all-rights p {
    color: #fff;
}

@media screen and (max-width: 768px) {
    .footer-area{
        max-width: 90vw;
        display: flex;
        justify-content: space-between;
        gap: 5rem;
    }
    .social-icons {
    gap: 1rem;
}
}
</style>