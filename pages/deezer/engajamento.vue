<template>
  <div :class="$style.page">
    <o-container :padding="false">
      <img :class="$style.image" src="/images/deezer-engajamento-1.jpg" alt="Engajamento 1" />
    </o-container>

    <o-container>
      <o-spacer bottom="24" />
      <o-text color="black" align="center" width="231">
        Ei, suas <strong>playlists personalizadas</strong> estão te esperando!
      </o-text>
      <o-spacer bottom="7" />
      <o-text color="black" align="center" width="231">
        Aumente o som, coloque a sua música favorita e vem com a gente!
      </o-text>
      <o-spacer bottom="7" />

      <o-grid cols="3" :data="[
        { text: 'Navegue no\naplicativo sem\ndescontar da\nsua internet!', fontSize: '14px' },
        { text: 'Pule de\nmúsicas\nquantas\nvezes quiser', fontSize: '14px' },
        { text: 'Acesso\na mais de\n73 milhões\nde músicas!', fontSize: '14px' },
      ]" />

      <o-spacer bottom="24" />
      <o-center>
        <o-button href="#" color="green">Acessar meu Deezer Go</o-button>
      </o-center>
      <o-spacer bottom="24" />
    </o-container>

    <o-container :padding="false">
      <hooper :wheel-control="false" :center-mode="true" :items-to-show="1.25" :style="{ height: 'auto' }">
        <slide :class="$style.hooper_slide">
          <img :class="$style.hooper_image" src="/images/deezer-engajamento-2.jpg" alt="Engajamento 2" />
        </slide>
        <slide :class="$style.hooper_slide">
          <img :class="$style.hooper_image" src="/images/deezer-engajamento-3.jpg" alt="Engajamento 2" />
        </slide>

        <hooper-pagination slot="hooper-addons" :class="$style.hooper_dots" />
      </hooper>
    </o-container>
  </div>
</template>
<script>
import { Hooper, Slide, Pagination as HooperPagination } from 'hooper';
import 'hooper/dist/hooper.css';

import OContainer from "../../components/o-container";
import OText from "../../components/o-text";
import OSpacer from "../../components/o-spacer";
import OGrid from "../../components/o-grid";
import OButton from "../../components/o-button";
import OCenter from "../../components/o-center";

export default {
  name: "TimEngajamento",
  layout: "default",
  components: {
    OCenter,
    OButton,
    OGrid,
    OSpacer,
    OText,
    Hooper,
    Slide,
    HooperPagination,

    OContainer
  },
}
</script>

<style>
:root {
  --sqr-degrees: -45deg;
  --sqr-primary: #65CF78;
  --sqr-secondary: #1EA3CC;
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
