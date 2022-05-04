<template>
  <NavBar />
  <router-view />
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import Productos from "@/components/Productos.vue";
import CartDetail from "@/components/CartDetail.vue";

export default {
  components: {
    NavBar,
    Productos,
    CartDetail,
  },
};
</script>

<style>

</style>
