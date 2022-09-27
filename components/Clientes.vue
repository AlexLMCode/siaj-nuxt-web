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
      <figure class="image__container">
        <img src="~/assets/clientes/crece.jpeg" alt="logo parroquia" />
      </figure>
      <figure class="image__container">
        <img src="~/assets/clientes/goldpets.jpeg" alt="logo goldpets" />
      </figure>
      <figure class="image__container">
        <img
          src="~/assets/clientes/delangel.jpeg"
          alt="logo del angel funeraria"
        />
      </figure>
      <figure class="image__container">
        <img src="~/assets/clientes/delipan.jpeg" alt="logo delipan" />
      </figure>
      <figure class="image__container">
        <img
          src="~/assets/clientes/cuauhtemoc.jpeg"
          alt="logo universidad cuauhtemoc"
        />
      </figure>
      <figure class="image__container">
        <img src="~/assets/clientes/moscati.jpeg" alt="logo moscati medico" />
      </figure>
      <figure class="image__container">
        <img src="~/assets/clientes/cadinda.jpeg" alt="logo cadinsa" />
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

.image__container img {
  max-height: 10rem;
}

@media screen and (min-width: 900px) {
  .image__container {
    margin-right: 3rem;
  }
}
</style>
