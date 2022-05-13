<template>
  <h1>Inicio</h1>
  <Productos/>
  <router-view />
  <!-- Campo de busqueda productos -->
  <input type="text" v-model="buscar" class="form-control" placeholder="Ejemplo: Charmander"/>
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