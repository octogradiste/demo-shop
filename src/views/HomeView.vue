<script>
import ShopItem from "../components/ShopItem.vue"

export default {
    //props: [items],
    components: {
        ShopItem
    }
}
</script>

<template>
<div class="shop">
    <div class="items-holder">
        <ShopItem 
            name="NIKE FREE"
            price="199.95"
            imageUrl="https://images.unsplash.com/photo-1542291026-7eec264c27ff?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80"
            imageBackgroundColor="rgba(201, 1, 27, 0.2)"
        />
        <ShopItem 
            name="Pink Soap"
            price="4.50"
            imageUrl="https://images.unsplash.com/photo-1589060040782-234fa4ee0b61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80"
            imageBackgroundColor="rgba(204, 166, 172, 0.2)"
        />
        <ShopItem 
            name="Pro Pen"
            price="12.05"
            imageUrl="https://images.unsplash.com/photo-1585336261022-680e295ce3fe?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80"
            imageBackgroundColor="rgba(119, 166, 168, 0.2)"
        />
    </div>
</div>
</template>

<style>
.shop {
    display: flex;
    justify-content: center;
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