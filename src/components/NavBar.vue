<script>
export default {
    props: ['title'],
    computed: {
        uppercasedTitle() {
            return this.title.toUpperCase();
        }
    }
}
</script>

<template>
    <div class="nav-banner">
        <span class="title">{{ uppercasedTitle }}</span>
    </div>
</template>

<style>
.nav-banner {
    display: flex;
    margin-bottom: 50px;
    justify-content: space-between;
    justify-self: stretch;
    align-items: center;
    padding: 18px 48px;
    background-color: rgb(16, 16, 16);
}

.title {
    color: white;
    font-size: 48px;
    letter-spacing: 5px;
    font-weight: 700;
}

.section {
    color: white;
    font-size: 28px;
}
</style>