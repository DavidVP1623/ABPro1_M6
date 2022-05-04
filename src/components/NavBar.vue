<template>
  <nav class="navbar navbar-expand-lg navbar-dark">
    <span class="navbar-brand m-3">Te lo vendo</span>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarNavAltMarkup"
      aria-controls="navbarNavAltMarkup"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div
      class="collapse navbar-collapse justify-content-end m-3"
      id="navbarNavAltMarkup"
    >
      <div class="navbar-nav">
        <a class="nav-item nav-link active" href=""
          ><router-link to="/">Inicio </router-link>
          <!--span
                        class="sr-only">(current)</span--></a
        >
         <a class="nav-item nav-link" href=""
          ><router-link to="/login">Contacto</router-link>
        </a>
      </div>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

<style>
.navbar{ 
background-color: #020924;
}

a:link, a:visited,  a:hover, a:active
{ 
    color: #fff;
    text-decoration: none;
}
</style>