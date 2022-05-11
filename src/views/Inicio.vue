<template>
  <h1>Inicio</h1>
  <Productos/>
      <router-view />

</template>

<script>
import Productos from "@/components/Productos.vue";
export default {
  components :{
    Productos,
  }
}
</script>

<style>

</style>
