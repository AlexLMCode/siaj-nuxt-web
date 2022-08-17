<template>
  <section id="contacto" class="contact">
    <div class="contact__container">
      <div class="contact__main">
        <div class="contact__info">
          <div class="contact__info--top">
            <p>contacto</p>
            <small
              >Envianos un mensaje, con gusto te <br />
              atenderemos.</small
            >
          </div>
          <!-- <div class="contact--info contact__info--tel">
            <p>Teléfono:</p>
            <div>
              <img src="~/assets/icons/phone-icon-pixel-perfect.svg" alt="" />
              <p>(52 55) 5488 61 00</p>
            </div>
          </div> -->
          <div class="contact--info contact__info--email">
            <p>Email:</p>
            <div>
              <img src="~/assets/icons/correo1.svg" alt="" />
              <p>asesoria@siaj.com.mx</p>
            </div>
          </div>
          <div class="contact--info contact__info--location">
            <p>Dirección:</p>
            <div>
              <img src="~/assets/icons/location-icon-freepik.svg" alt="" />
              <p>Oficinas en Boca del Río, Veracruz.</p>
            </div>
          </div>
        </div>
        <div class="contact__form">
          <form
            action="https://formspree.io/f/xvovzjnr"
            class="form__container"
            method="POST"
          >
            <div>
              <label for="nombre">
                <input
                  id="nombre"
                  type="text"
                  placeholder="NOMBRE"
                  required
                  autocomplete="name"
                  name="nombre"
                />
              </label>
            </div>
            <div>
              <label for="email">
                <input
                  id="email"
                  type="email"
                  placeholder="E-MAIL"
                  required
                  autocomplete="email"
                  name="email"
                />
              </label>
            </div>
            <div>
              <label for="telefono">
                <input
                  id="telefono"
                  type="tel"
                  placeholder="TELEFONO"
                  autocomplete="tel"
                  name="telefono"
                />
              </label>
            </div>
            <div>
              <label for="enterado">
                ¿Cómo te enteraste de nosotros?
                <input list="enterado" />
                <datalist id="enterado">
                  <option value="Redes-Sociales"></option>
                  <option value="Anuncio"></option>
                  <option value="Sitio-Web"></option>
                  <option value="Recomendaciones"></option>
                  <option value="Otro"></option>
                </datalist>
              </label>
            </div>
            <div>
              <label for="mensaje">
                ¿Cual es tu pregunta?
                <textarea
                  id="mensaje"
                  name="mensaje"
                  cols="30"
                  rows="10"
                  required
                ></textarea>
              </label>
            </div>
            <input type="submit" value="Enviar" class="send" />
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.contact {
  background-image: url('~assets/photos/contact-bg-jawadur-rahman-srijon.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
  height: 100rem;
  width: 100%;
}

.contact__container {
  background-color: #fff;
  position: absolute;
  padding: 3rem;
  height: 90%;
  width: 90%;
  right: 5%;
  top: 5%;
}

.contact__main {
  display: flex;
  width: 100%;
  height: 100%;
  flex-wrap: wrap;
  justify-content: space-around;
}

.contact__info {
  height: auto;
}

.contact__form {
  height: auto;
}

.contact__info--top {
  margin-bottom: 1rem;
}

.contact__info--top p {
  font-size: 2rem;
  font-weight: bold;
  text-transform: uppercase;
  margin-bottom: 0.5rem;
}

.contact__info--top small {
  color: #626262;
  font-size: 1.2rem;
}

.contact--info {
  display: flex;
  height: 5rem;
  flex-direction: column;
  justify-content: space-around;
  margin-bottom: 2rem;
}

.contact--info > p {
  color: var(--main-color);
  font-weight: 400;
  font-size: 1.3rem;
}

.contact--info > div {
  display: flex;
  align-items: center;
  width: 65%;
  text-decoration: underline;
}

.contact--info img {
  margin-right: 1rem;
}

.send {
  cursor: pointer;
}

/*FORM*/

textarea:focus,
input:focus {
  outline: none;
}

.form__container {
  display: flex;
  flex-direction: column;
  height: 100%;
  justify-content: space-around;
}

input {
  border: none;
  border-bottom: 0.3rem solid var(--main-color);
  width: 100%;
  height: 5rem;
}

textarea {
  border: none;
  border-bottom: 0.3rem solid var(--main-color);
  width: 100%;
}
</style>
