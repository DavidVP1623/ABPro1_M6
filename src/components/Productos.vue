<template>

<!-- BUSCADOR SACADO DE LA PAGINA DE POKEMONES QUE SE VEIA GASTON ASI QUE SI DICE ALGO DE POKEMONES EN LOS COMENTARIOS, ES POR ESO -->
   <div class="container cont">
    <div class="row">
      <div class="col-md-12">     
            <h2 class="text-center mb-3">Productos en venta</h2>
 
        <input type="text" v-model="buscar" class="form-control" placeholder="Buscar"/>              

      </div>
    </div>

    <div class="row mt-3">
      <div class="col-md-4" v-for="item in items" v-bind:key="item.id"> 
        <div class="card mb-3">
          <!-- METODO NUEVO QUE MUESTRA LA IMAGEN, LE HACE UN METODO Y UN REQUIRE EN LA LINEA 80 -->
          <img class="card-img-top" :src="imagenProdu(item.img)" :alt="item.nombre"/>

          <!-- METODO ANTIGUO QUE USABAMOS Y QUE NO AGARRABA LAS IMAGENES -->
          <!-- <img class="card-img-top" :src="'/img' + item.img" v-bind:alt="item.nombre"/> -->

          <div class="card-body">
            <h3 class="card-title mb-3">{{ item.nombre }}</h3>
            <p class="card-text"><strong>Precio:</strong> {{ item.precio }}</p>
          </div>
          <button type="button" class="btn btn-primary btn-sm">
          Agregar Favorito
        </button>
        <button
          type="button"
          class="btn btn-secondary btn-sm"
          data-toggle="modal"
          data-target="#exampleModal"
        >
          Descripción
        </button>
        </div>

      </div>

    </div>

   </div>



</template>


<script>


import datos from "../assets/json/productos.json";

export default {

  // Exporto mi componente 'Pokemones' 
  name: 'Productos',
  props: {
    msg: String
  },
  
  // declaro el elemento buscar 
  data() {
    return {
      buscar: ''
    }
  },
    
  // Creo un método llamado 'items' y obtengo los datos de los pokemones
  // Asimismo filtro la búsqueda de los pokemones con el método filter()  
  computed: {
    items() {
      return datos.filter(item => {
        return item.nombre.toLowerCase().includes(this.buscar.toLowerCase());
      });
    },
  },
  // METODO SACADO DE https://medium.com/@dmitrymind/how-to-keep-array-data-inside-local-json-file-for-vue-app-46bb29d4ac53
  methods: {
    imagenProdu: function(img) {
      return require("@/" + img);
    },
  },
  
}



</script>