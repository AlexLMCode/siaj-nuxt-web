<template>
  <main>
    <section id="firma" class="section section__firma">
      <p class="section__title">la firma</p>
      <div class="section__separator"></div>
      <p class="section__description">
        SIAJ ABOGADOS es un Corporativo con amplia experticia dentro de la
        Asesoría Jurídica integral en el Derecho Mexicano. Con más de 50 años de
        trayectoria, siendo reconocida por el alto nivel de compromiso e índice
        de éxito dentro de los conflictos de los clientes que representa.
      </p>
    </section>

    <section id="servicios" class="section section__servicios">
      <p class="section__title">servicios juridicos</p>
      <div class="section__separator"></div>
      <p class="section__description">
        Nos especializamos en diversas ramas del derecho, contando con
        reconocidos Abogados con amplia experiencia dentro de sus respectivas
        áreas para poder proporcionar servicios jurídicos y soluciones a las
        controversias, asesorando a reconocidas empresas nacionales e
        internacionales.
      </p>
    </section>

    <section class="section__icons">
      <div class="service__component">
        <NuxtLink to="/services/mercantil">
          <figure class="service__component__icon" title="made by freepik">
            <img
              src="~/assets/icons/services/mercantil-freepik.svg"
              alt="imagen"
            />
          </figure>
          litigio mercantil
        </NuxtLink>
      </div>
      <div class="service__component">
        <NuxtLink to="/services/penal">
          <figure class="service__component__icon" title="made by freepik">
            <img src="~/assets/icons/services/penal-freepik.svg" alt="imagen" />
          </figure>
          litigio penal
        </NuxtLink>
      </div>
      <div class="service__component">
        <NuxtLink to="/services/intelectual">
          <figure class="service__component__icon" title="made by freepik">
            <img
              src="~/assets/icons/services/intelectual-eucalyp.svg"
              alt="imagen"
            />
          </figure>
          propiedad intelectual
        </NuxtLink>
      </div>
      <div class="service__component">
        <NuxtLink to="/services/civil">
          <figure class="service__component__icon" title="made by freepik">
            <img src="~/assets/icons/services/civil-freepik.svg" alt="imagen" />
          </figure>
          litigio civil
        </NuxtLink>
      </div>
      <div class="service__component">
        <NuxtLink to="/services/administrativo">
          <figure class="service__component__icon" title="made by eucalyp">
            <img
              src="~/assets/icons/services/administrativo-eucalyp.svg"
              alt="imagen"
            />
          </figure>
          litigio administrativo
        </NuxtLink>
      </div>
      <div class="service__component">
        <NuxtLink to="/services/familiar">
          <figure class="service__component__icon" title="made by freepik">
            <img
              src="~/assets/icons/services/familiar-freepik.svg"
              alt="imagen"
            />
          </figure>
          litigio familiar
        </NuxtLink>
      </div>
      <div class="service__component">
        <NuxtLink to="/services/laboral">
          <figure class="service__component__icon" title="made by freepik">
            <img
              src="~/assets/icons/services/laboral-freepik.svg"
              alt="imagen"
            />
          </figure>
          litigio laboral
        </NuxtLink>
      </div>
      <div class="service__component">
        <NuxtLink to="/services/fiscal">
          <figure class="service__component__icon" title="made by freepik">
            <img
              src="~/assets/icons/services/fiscal-freepik.svg"
              alt="imagen"
            />
          </figure>
          litigio fiscal
        </NuxtLink>
      </div>
      <div class="service__component">
        <NuxtLink to="/services/bancario">
          <figure class="service__component__icon" title="made by smartline">
            <img
              src="~/assets/icons/services/bancario-smartline.svg"
              alt="imagen"
            />
          </figure>
          litigio bancario
        </NuxtLink>
      </div>
      <div class="service__component">
        <NuxtLink to="/services/inmobiliario">
          <figure
            class="service__component__icon"
            title="made by photo3idea_studio"
          >
            <img
              src="~/assets/icons/services/inmobiliario-photo3idea_studio.svg"
              alt="imagen"
            />
          </figure>
          litigio inmobiliario
        </NuxtLink>
      </div>
    </section>
  </main>
</template>

<script>
export default {};
</script>

<style>
main {
  width: 85vw;
  margin: 0 auto;
}

.section {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: auto;
  margin-top: 5rem;
  margin-bottom: 10rem;
  text-align: center;
}

.section__title {
  font-weight: var(--heading-weight);
  font-size: var(--heading-size);
  text-transform: uppercase;
  margin-bottom: 2rem;
}

.section__separator {
  height: 0.3rem;
  width: 50%;
  background-color: var(--main-color);
  margin-bottom: 2rem;
}

.section__description {
  font-size: 1.6rem;
  text-align: center;
  max-width: 70rem;
}

/*ICONS*/

.section__icons {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  width: 100%;
}

.service__component {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: auto;
  margin-bottom: 5rem;
  min-width: 15rem;
}

.service__component__icon {
  margin-bottom: 2rem;
}

.service__component a {
  text-transform: uppercase;
  font-size: 1.3rem;
  font-style: italic;
  color: black;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
