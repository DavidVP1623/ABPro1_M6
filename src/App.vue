<template>
  <NavBar/> 
  <CartDetail/>
    <router-view />
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import CartDetail from "@/components/CartDetail.vue";

export default {
  components: {
    NavBar,
    CartDetail,
  },
};
</script>

<style>

</style>
