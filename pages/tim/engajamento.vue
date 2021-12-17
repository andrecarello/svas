<template>
  <div :class="$style.page">
    <o-container :padding="false">
      <img :class="$style.image" src="/images/engajamento-1.jpg" alt="Engajamento 1" />
    </o-container>

    <o-spacer bottom="6" />
    <o-container>

      <div :class="$style.discount">
        <o-text align="center" color="black">
          Já conferiu as novas ofertas do TIM + Vantagens? Então corre no App que tá cheio de <strong>desconto exclusivo</strong> esperando por você!
          E ainda:
        </o-text>

        <img :class="$style.discount_image" src="/images/engajamento-4.jpg" alt="Engajamento 4" />
      </div>

      <o-spacer bottom="8" />
      <o-grid :data="[
        { text: 'Ganhe descontos e pacotes de internet;', fontSize: '14px' },
        { text: 'Sorteios semanais de prêmios incríveis;', fontSize: '14px' },
        { text: 'Sempre um desconto novo exclusivo para você!', fontSize: '14px' }
      ]">
      </o-grid>

      <o-spacer bottom="24" />
      <o-button color="green" :center="true">Acessar o TIM+</o-button>

    </o-container>

    <o-spacer bottom="16" />
    <o-container :padding="false">
      <hooper :center-mode="true" :items-to-show="1.25" :wheel-control="false" :style="{ height: 'auto' }">
        <slide :class="$style.hooper_slide">
          <img :class="$style.hooper_image" src="/images/engajamento-2.jpg" alt="Engajamento 2" />
        </slide>
        <slide :class="$style.hooper_slide">
          <img :class="$style.hooper_image" src="/images/engajamento-3.jpg" alt="Engajamento 3" />
        </slide>

        <hooper-pagination slot="hooper-addons" :class="$style.hooper_dots" />
      </hooper>
    </o-container>
  </div>
</template>
<script>
import { Hooper, Slide, Pagination as HooperPagination } from 'hooper';
import 'hooper/dist/hooper.css';

import OButton from "../../components/o-button";
import OContainer from "../../components/o-container";
import OText from "../../components/o-text";
import OSpacer from "../../components/o-spacer";
import OGrid from "../../components/o-grid";

export default {
  name: "TimEngajamento",
  layout: "default",
  components: {
    Hooper,
    Slide,
    HooperPagination,

    OGrid,
    OSpacer,
    OText,
    OButton,
    OContainer
  },
}
</script>

<style>
:root {
  --sqr-degrees: 180deg;
  --sqr-primary: var(--color-blue-500);
  --sqr-secondary: var(--color-blue-800);
}
</style>
<style module>
.page {
  background-color: var(--color-white);
  padding-bottom: 16px;
  flex-grow: 1;
}

.image {
  display: block;
  width: 100%;
}

.discount {
  display: flex;
}
.discount_image {
  max-width: 100px;
  width: 100%;
  display: block;
  object-fit: contain;
}

@media only screen and (min-width: 414px) {
  .discount {
    display: flex;
    align-items: center;
  }
  .discount_image {
    max-width: 149px;
  }
}

/* HOOPER STYLE */
.hooper_slide {
  padding: 0 10px;
}
.hooper_image {
  display: block;
  width: 100%;
  max-width: 366px;
}
.hooper_dots {
  position: relative;

  display: flex;
  justify-content: center;
  gap: 5px;
}

.hooper_dots button {
  height: 8px;
  width: 8px;
  border: 1px solid #000000;
}
</style>
<style>
.hooper-indicators .is-active {
  background-color: #000000;
}
</style>
