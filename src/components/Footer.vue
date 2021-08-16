<template>
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
</template>

<script>
export default {

}
</script>

<style>
.footer-area {
    padding: 2rem 0;
    max-width: 60vw;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.social-icons {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 2rem;
}

.social-icons p {
    font-size: 20px;
}

.social-icons i {
    font-size: 20px;
    padding: .5rem;
    border: 1px solid black;
    cursor: pointer;
}

@media screen and (max-width: 768px) {
    .footer-area {
        padding: .5rem 0;
        max-width: 90vw;
        margin: 1rem auto;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    .all-rights{
        text-align: right;
    }
    .social-icons {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .social-icons p {
        font-size: 15px;
    }
    .social-icons i {
        font-size: 20px;
        padding: .1rem .3rem;
        border: 1px solid black;
        cursor: pointer;
    }
}
</style>