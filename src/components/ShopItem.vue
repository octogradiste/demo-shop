<script>
export default {
    props: ['name', 'price', 'imageUrl' , 'imageBackgroundColor'],
    computed: {
        annotatedPrice() {
            return this.price + " CHF";
        },
        imageStyle() {
            return {
                backgroundColor : this.imageBackgroundColor,
            };
        }
    }
}
</script>

<template>
    <div class="card">
        <img :src="imageUrl" :alt="name" :style="imageStyle">
        <div class="banner">
            <span class="label">{{ name }}</span>
            <span class="label">{{ annotatedPrice }}</span>
        </div>
    </div>
</template>

<style>
img {
    width: 500px;
    height: 500px;
    object-fit: contain;
    margin: 0px;
    padding: 0px;
    display: block;
}

.card {
    width: 500px;
    border-radius: 24px;
    overflow: hidden;
    box-shadow: 6px 6px 6px rgba(0, 0, 0, 0.4);
}

.banner {
    background-color: rgb(16, 16, 16);
    width: 500px;
    display: flex;
    justify-content: space-between;
}

.label {
    color: white;
    padding: 18px;
    font-size: 24px;
}
</style>