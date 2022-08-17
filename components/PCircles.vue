<template>
  <section class="section section__circles">
    <p class="section__title">su problema en buenas manos</p>
    <div class="section__separator"></div>
    <p class="section__circles__subtitle">
      Un 95% de probabilidad de ganar su caso:
    </p>
    <div class="circles">
      <div class="box">
        <div class="percent">
          <svg>
            <circle cx="70" cy="70" r="70"></circle>
            <circle cx="70" cy="70" r="70"></circle>
          </svg>
          <div class="number">
            <h2>85<span>%</span></h2>
          </div>
        </div>
        <p class="text">ganados</p>
        <small>judicialmente</small>
      </div>
      <div class="box box2">
        <div class="percent">
          <svg>
            <circle cx="70" cy="70" r="70"></circle>
            <circle cx="70" cy="70" r="70"></circle>
          </svg>
          <div class="number">
            <h2>10<span>%</span></h2>
          </div>
        </div>
        <p class="text">acuerdos favorables</p>
        <small>extrajudiciales</small>
      </div>
      <div class="box box3">
        <div class="percent">
          <svg>
            <circle cx="70" cy="70" r="70"></circle>
            <circle cx="70" cy="70" r="70"></circle>
          </svg>
          <div class="number">
            <h2>5<span>%</span></h2>
          </div>
        </div>
        <p class="text">desfavorables</p>
        <small>se reducirán a 1%</small>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.section__circles {
  margin-bottom: 10rem;
  margin-top: 5rem;
}

.section__circles__subtitle {
  color: rgba(0, 0, 0, 0.6);
  font-size: 1.6rem;
  font-style: italic;
}

.circles {
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
  width: 100%;
}

.box {
  position: relative;
  width: 25rem;
  height: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: 3rem;
}

.box .percent {
  position: relative;
  width: 15rem;
  height: 15rem;
}

.box .percent svg {
  position: relative;
  width: 15rem;
  height: 15rem;
}

.box .percent svg circle {
  width: 15rem;
  height: 15rem;
  fill: none;
  stroke-width: 10;
  stroke: #000;
  transform: translate(0.5rem, 0.5rem);
  stroke-dasharray: 440;
  stroke-dashoffset: 440;
  stroke-linecap: round;
}

.box .percent svg circle:nth-child(1) {
  stroke-dashoffset: 0;
  stroke: #f3f3f3;
}

.box .percent svg circle:nth-child(2) {
  stroke-dashoffset: calc(440 - (440 * 85) / 100);
  stroke: var(--main-color);
}

.box .percent .number {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  color: black;
}

.box .percent .number h2,
span {
  font-size: 2rem;
}

.box p {
  font-size: 2rem;
  font-style: italic;
  text-transform: uppercase;
  margin-top: 2rem;
}

.box small {
  font-style: italic;
  text-transform: capitalize;
  color: rgba(0, 0, 0, 0.6);
  font-size: 1.5rem;
}

.box2 .percent svg circle:nth-child(2) {
  stroke-dashoffset: calc(440 - (440 * 10) / 100);
  stroke: var(--main-color);
}

.box3 .percent svg circle:nth-child(2) {
  stroke-dashoffset: calc(440 - (440 * 5) / 100);
  stroke: var(--main-color);
}

@media screen and (min-width: 900px) {
  .box .percent .number {
    top: -5px;
    left: -5px;
  }
}
</style>
