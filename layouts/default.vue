<template>
  <div :class="$style.layout">
    <o-nav />
    <nuxt />

    <div :class="$style.footer">
      <tim />
    </div>
  </div>
</template>
<script>
import ONav from "../components/o-nav";
import Tim from "../components/brands/tim";
export default {
  name: "LayoutDefault",
  components: {
    Tim,
    ONav
  }
}
</script>
<style>
:root {
  --color-blue-100: hsl(213.2, 100%, 90%);
  --color-blue-200: hsl(213.2, 100%, 80%);
  --color-blue-300: hsl(213.2, 100%, 70%);
  --color-blue-400: hsl(213.2, 100%, 60%);
  --color-blue-500: hsl(213.2, 100%, 50%);
  --color-blue-600: hsl(213.2, 100%, 40%);
  --color-blue-700: hsl(213.2, 100%, 30%);
  --color-blue-800: hsl(213.2, 100%, 20%);
  --color-blue-900: hsl(213.2, 100%, 10%);

  --color-secondary: #30A500;
  --color-white: #ffffff;
  --color-black: #000000;

  --container-width: 454px;
}

@font-face {
  font-family: Tim Sans;
  font-style: normal;
  font-weight: 400;
  font-display: swap;
  src: url("/fonts/TIMSansWeb-Regular.woff") format("woff")
}

@font-face {
  font-family: Tim Sans;
  font-style: normal;
  font-weight: 900;
  font-display: swap;
  src: url("/fonts/TIMSansWeb-Heavy.woff") format("woff")
}

html {
  position: relative;
}

html, body {
  min-height: 100vh;
  width: 100%;
  background-color: var(--color-blue-800);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Tim Sans, ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,"Noto Sans",sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol","Noto Color Emoji";
}
</style>

<style module>
.layout {
  position: relative;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60px;
  background-color: var(--color-blue-800);
}
</style>
