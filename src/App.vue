<script>
import HomeView from "./views/HomeView.vue"

export default {
  components: {
    HomeView
  },
  data() {
    return {
      items: [
        {
          name: "NIKE FREE",
          price: "199.95",
          imageUrl: "https://images.unsplash.com/photo-1542291026-7eec264c27ff?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80",
          imageBackgroundColor: "rgba(201, 1, 27, 0.2)",
        },
        {
          name: "Pink Soap",
          price: "4.50",
          imageUrl: "https://images.unsplash.com/photo-1589060040782-234fa4ee0b61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80",
          imageBackgroundColor: "rgba(204, 166, 172, 0.2)",

        },
        {
          name: "Pro Pen",
          price: "12.05", 
          imageUrl: "https://images.unsplash.com/photo-1585336261022-680e295ce3fe?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80",
          imageBackgroundColor: "rgba(119, 166, 168, 0.2)",
        },
      ]
    }
  }
}
</script>

<template>
  <HomeView :items="[...items, ...items]"/>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
html {
  font-family: 'Roboto', sans-serif;
}

body {
  padding: 0px;
  margin: 0px;
}
</style>