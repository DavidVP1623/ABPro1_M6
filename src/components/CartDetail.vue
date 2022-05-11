<template>
  <div class="container mb-5">
    <h2 class="text-center mb-3">Productos</h2>
    <div class="row justify-content-center">
      <div
        class="card col-6 col-sm-2 m-3 p-0"
        v-for="(item, index) in results"
        :key="index"
      >
        <div class="card-body">
          <h5 class="card-title">{{ item.name }}</h5>
          <p>{{ item.status }}</p>
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
      result: null,
    };
  },

  mounted() {
    fetch("https://rickandmortyapi.com/api/character")
      .then((res) => res.json())
      .then((data) => (this.result = data.results));
  },
};
</script>


