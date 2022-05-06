<template>
  <div class="container mb-5">
                  <h2 class="text-center mb-3">Productos</h2>
    <div class="row justify-content-center">
      <div
        class="card col-6 col-sm-2 m-3 p-0">
        <div class="card-body">
            <div>
              

          <h5 class="card-title">{{ item.nombre }}</h5>
          <p>{{ item.precio }}</p>
          <!--p class="card-text">Origen: {{ item.origin.name }}</p-->
        </div>
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
          imagen: 'https://http2.mlstatic.com/D_NQ_NP_723352-MLC45457658172_042021-O.webp',
          precio: 1000,
        },
        {
          id: 2,
          nombre: "Producto2",
          imagen: "../assets/imagen2.jpg",
          precio: 2000,
        },
        {
          id: 3,
          nombre: "Producto3",
          imagen: "../assets/imagen3.jpg",
          precio: 3000,
        },
        {
          id: 4,
          nombre: "Producto4",
          imagen: "../assets/imagen4.jpg",
          precio: 4000,
        },
        {
          id: 5,
          nombre: "Producto5",
          imagen: "../assets/imagen5.jpg",
          precio: 3000,
        },
        {
          id: 6,
          nombre: "Producto6",
          imagen: "../assets/imagen6.jpg",
          precio: 3000,
        },
      ], //Array que recorreremos
    };
  },
};
</script>