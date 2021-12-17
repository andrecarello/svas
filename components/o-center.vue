<template>
  <div :class="$style.center"><slot /></div>
</template>
<script>
export default {
  name: "OCenter"
}
</script>
<style module>
.center {
  display: flex;
  justify-content: center;
}
</style>
