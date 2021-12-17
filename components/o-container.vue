<template>
  <div :class="[ $style.container, padding && $style.padding ]"><slot /></div>
</template>
<script>
export default {
  name: "OContainer",
  props: {
    padding: { type: Boolean, default: true }
  }
}
</script>
<style module>
.container {
  width: 100%;
  max-width: var(--container-width);
  margin: 0 auto;
  position: relative;
}
.padding {
  padding: 0 20px;
}
</style>
