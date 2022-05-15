<script>
import ShopItem from "../components/ShopItem.vue"
import NavBar from "../components/NavBar.vue"

export default {
    props: ['items'],
    components: {
        ShopItem,
        NavBar
    }
}
</script>

<template>
    <NavBar title="The Vue Shop" />
    <div class="shop">
        <div class="items-holder">
            <ShopItem v-for="item in items" 
                :name="item.name"
                :price="item.price"
                :imageUrl="item.imageUrl"
                :imageBackgroundColor="item.imageBackgroundColor"/>
        </div>
    </div>
</template>

<style>
.shop {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
}
.items-holder {
    display: grid;
    grid-template-columns: repeat(2, 500px);
    gap: 50px;
}

@media (min-width: 1650px) {
    .items-holder {
        grid-template-columns: repeat(3, 500px);
    }
}

@media (max-width: 1100px) {
    .items-holder {
        grid-template-columns: 500px;
    }

}
</style>