<template>
  <div :class="$style.page">
    <o-container :padding="false">
      <hooper style="height: 168px" :wheel-control="false" :auto-play="true" :play-speed="4000">
        <slide>
          <img :class="$style.image" src="/images/incentivo-1.jpg" alt="Incentivo 1" />
        </slide>
        <slide>
          <img :class="$style.image" src="/images/incentivo-2.jpg" alt="Incentivo 2" />
        </slide>
      </hooper>
    </o-container>
    <o-container>
      <o-spacer top="-25" />
      <o-button href="#" download="true" color="green" :center="true">Baixar o TIM+</o-button>
      <o-spacer bottom="24" />

      <o-text align="center" width="320">
        No TIM + Vantagens, clientes TIM Pré e Controle
        ganham fichas para trocar por benefícios incríveis!
      </o-text>
      <o-text align="center" width="260">
        Para começar a economizar, baixe o APP
        e se cadastre gratuitamente! Confira
        alguma das vantagens:
      </o-text>

      <o-spacer bottom="24" />

      <o-grid cols="3" :data="[
        { text: 'Baixe o App e ganhe fichas de boas-vindas para dar start na economia.', fontSize: '12px' },
        { text: 'Sorteios semanais de prêmios incríveis.', fontSize: '14px' },
        { text: 'Sempre um desconto novo exclusivo para você!', fontSize: '13px' }
      ]">
      </o-grid>

      <o-spacer bottom="24" />
      <o-button href="#" download="true" color="green" :center="true">Baixar o TIM+</o-button>

      <o-spacer bottom="24" />
      <o-text align="center">
        Seu acesso aos descontos é liberado<br />
        automaticamente e você não paga<br />
        nada a mais por isso! Tá esperando o que?<br />
        Venha economizar!
      </o-text>
    </o-container>
  </div>
</template>
<script>
import { Hooper, Slide } from 'hooper';
import 'hooper/dist/hooper.css';

import OButton from "../../components/o-button";
import OContainer from "../../components/o-container";
import OText from "../../components/o-text";
import OSpacer from "../../components/o-spacer";
import OGrid from "../../components/o-grid";

export default {
  name: "TimIncentivo",
  layout: "default",
  components: {
    Hooper,
    Slide,

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
  background-color: var(--color-blue-800);
  flex-grow: 1;
}

.image {
  display: block;
  width: 100%;
  border-bottom-left-radius: 30px;
  border-bottom-right-radius: 30px;
}
</style>
