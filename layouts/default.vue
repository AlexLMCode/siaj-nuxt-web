<template>
  <div>
    <Nuxt />
    <PFooter />
  </div>
</template>

<script>
import PFooter from '~/components/PFooter';

export default {
  components: { PFooter },
};
</script>

<style>
/*GLOBAL STYLES*/
:root {
  --main-color: #a5a07b;
  --dark-color: #322715;
  --heading-size: 3rem;
  --heading-weight: bold;
  --light-gray: rgba(196, 196, 196, 0.19);
}

/*FONTS:
Light 300
Regular 400
Regular 400 italic
Bold 700
Bold 700 italic
*/

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Lato', sans-serif;
}

html {
  font-size: 62.5%;
}

body {
  overflow-x: hidden;
}

@media screen and (min-width: 900px) {
  html {
    font-size: 70%;
  }

  .hero__nav__icon {
    display: none;
  }

  .hero__menu {
    display: flex;
    justify-content: space-evenly;
    flex-direction: row;
    align-items: center;
    position: static;
    background-color: initial;
    z-index: 0;
    width: auto;
    height: auto;
  }

  .hero__menu li {
    margin-right: 2rem;
  }

  .hero__nav {
    flex-direction: row;
    width: 90vw;
    margin-right: auto;
    margin-left: auto;
    justify-content: space-between;
  }

  .box .percent .number {
    top: -5px;
    left: -5px;
  }

  .contact {
    height: 60rem;
  }

  .contact__main {
    flex-direction: row;
  }

  .contact__info {
    width: 40%;
    height: 100%;
  }

  .contact__form {
    width: 60%;
    height: 100%;
  }
}
</style>
