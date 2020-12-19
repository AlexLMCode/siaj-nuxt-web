<template>
  <section class="clientes">
    <section id="clientes" class="section section__clientes">
      <p class="section__title">clientes</p>
      <div class="section__separator"></div>
      <p class="section__description">
        Algunas de las empresas a las que representamos
      </p>
    </section>
    <div class="clientes__container">
      <figure class="image__container">
        <img src="~/assets/clientes/logo-berllano.jpg" alt="logo berllano" />
      </figure>
      <figure class="image__container">
        <img src="~/assets/clientes/logo-fasti.jpg" alt="logo fasti" />
      </figure>
      <figure class="image__container">
        <img src="~/assets/clientes/logo-parroquia.jpg" alt="logo parroquia" />
      </figure>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="css" scoped>
.clientes {
  width: 85vw;
  margin: 0 auto;
}

.clientes__container {
  width: 100%;
  height: auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.image__container {
  margin-bottom: 5rem;
}

@media screen and (min-width: 900px) {
  .image__container {
    margin-right: 3rem;
  }
}
</style>
