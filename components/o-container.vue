<template>
  <div :class="$style.container"><slot /></div>
</template>
<script>
export default {
  name: "OContainer"
}
</script>
<style module>
.container {
  width: 100%;
  max-width: var(--container-width);
  margin: 0 auto;
  padding: 0 20px;
}
</style>
