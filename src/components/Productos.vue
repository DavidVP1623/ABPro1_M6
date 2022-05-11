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
            v-bind:src="item.url"
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
          url: "https://s3.amazonaws.com/imagenes-sellers-mercado-ripley/2022/02/13140836/M196-Mockup-Mousepad-Rick-and-Morty-V2.jpg",
          precio: 1000,
        },
        {
          id: 2,
          nombre: "Producto2",
          url: "data:image/jpeg;base64,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",
          precio: 2000,
        },
        {
          id: 3,
          nombre: "Producto3",
          url: "https://www.abcdin.cl/media/catalog/product/1/1/1151050f13_1.jpg",
          precio: 3000,
        },
        {
          id: 4,
          nombre: "Producto4",
          url: "https://cdn-tienda-media.chaco.gob.ar/pub/media/catalog/product/cache/baf65dd7884a65f78edeaa7cc9c4d12e/m/o/mouse_genius_ialambrico_nx-7000.jpg",
          precio: 4000,
        },
        {
          id: 5,
          nombre: "Producto5",
          url: "https://images.locanto.cl/Audifonos-Gamer-Kolke-Dark-KGA-472-Kolke/vap_5178100798.jpg",
          precio: 3000,
        },
        {
          id: 6,
          nombre: "Producto6",
          url: "@srcassetsimagen6.jpg",
          precio: 3000,
        },
      ],
    };
  },
};
</script>