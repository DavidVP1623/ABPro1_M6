<template>
  <div class="container mb-5">
    <h2 class="text-center mb-3">Productos</h2>
    <div class="row justify-content-center">
      <div
        class="card col-6 col-sm-2 m-3 p-0"
        v-for="(item, index) in productos"
        :key="index"
      >
        <div class="card-body">
          <h5 class="card-title">{{ item.id }} {{ item.nombre }}</h5>

          <p>{{ item.precio }}</p>
          <img
            class="card-img-top"
            v-bind:src="item.image"
            v-bind:alt="item.name"
          />
          <!--p class="card-text">Origen: {{ item.origin.name }}</p-->
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
</template>


<script>
export default {
  data() {
    return {
      productos: [
        {
          id: 1,
          nombre: "Producto1",
          image: require('../assets/imagen1.jpg'),
          precio: 1000,
        },
        {
          id: 2,
          nombre: "Producto2",
          image: require('../assets/imagen2.jpg'),
          precio: 2000,
        },
        {
          id: 3,
          nombre: "Producto3",
          image: require('../assets/imagen3.jpg'),
          precio: 3000,
        },
        {
          id: 4,
          nombre: "Producto4",
          image: require('../assets/imagen4.jpg'),
          precio: 4000,
        },
        {
          id: 5,
          nombre: "Producto5",
          image: require('../assets/imagen5.jpg'),
          precio: 3000,
        },
        {
          id: 6,
          nombre: "Producto6",
          image: require('../assets/imagen6.jpg'),
          precio: 3000,
        },
      ],
    };
  },
};
</script>