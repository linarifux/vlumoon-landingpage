<template>
    <div class="feature-icon">
        <div class="icon-area">
            <fa :icon="data.icon" class="icon" />
        </div>
        <h3>{{data.title}}</h3>
        <p>{{data.text}}</p>
    </div>
</template>

<script>
export default {
    props: ['data']
}
</script>

<style>
.icon-area {
    background: #000;
    display: inline-block;
    padding: 10px;
    border-radius: 100px;
    margin: 1rem 0;
}

.icon {
    font-size: 100px;
    background: #fff;
    padding: 20px;
    border-radius: 100px;
}

.feature-icon h3 {
    margin-bottom: 1rem;
}

.feature-icon p {
    letter-spacing: 1px;
}
</style>