<template>
  <div :class="$style.page">
    <o-container :padding="false">
      <img :class="$style.image" src="/images/deezer-incentivo.jpg" alt="Deezer Incentivo" />

    </o-container>
    <o-container>
      <o-spacer bottom="-25" />
      <o-center>
        <o-button href="#" color="green">Liberar meu Deezer Go</o-button>
      </o-center>

      <o-spacer bottom="24" />
      <o-text align="center" width="320">
        A gente ama música, né?<br />
        E nada melhor do que o Deezer Go<br />
        para curtir muito som.
      </o-text>

      <o-spacer bottom="16" />
      <o-text align="center" width="320">
        Confira as vantagens da parceria<br />
        entre a TIM e o Deezer Go:
      </o-text>

      <o-spacer bottom="8" />
      <o-grid :data="[
        { text: 'Navegue no\naplicativo sem\ndescontar da\nsua internet!', fontSize: '14px' },
        { text: 'Pule de\nmúsicas\nquantas\nvezes quiser', fontSize: '14px' },
        { text: 'Acesso\na mais de\n73 milhões\nde músicas!', fontSize: '14px' }
      ]">
      </o-grid>

      <o-spacer bottom="24" />
      <o-center>
        <o-button href="#" color="green">Baixar o Deezer</o-button>
      </o-center>
      <o-spacer bottom="27" />

      <o-text align="center" width="324">
        Aproveite já essa vantagem exclusiva
        TIM e garanta <strong>mais música no seu dia.</strong>
      </o-text>
    </o-container>
  </div>
</template>
<script>
import OContainer from "../../components/o-container";
import OCenter from "../../components/o-center";
import OSpacer from "../../components/o-spacer";
import OButton from "../../components/o-button";
import OText from "../../components/o-text";
import OGrid from "../../components/o-grid";

export default {
  name: "DeezerIncentivo",
  components: {
    OGrid,
    OText,
    OButton,
    OSpacer,
    OContainer,
    OCenter
  }
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
  flex-grow: 1;
}
.image {
  display: block;
  width: 100%;
  border-bottom-right-radius: 35px;
  border-bottom-left-radius: 35px;
}
</style>
