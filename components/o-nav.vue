<template>
  <div :class="$style.nav">
    <div :class="$style.container">
      <tim />
    </div>
  </div>
</template>
<script>
import Tim from "./brands/tim";

export default {
  name: "ONav",
  components: {
    Tim
  },
}
</script>
<style module>
.nav {
  background-color: var(--color-blue-800);
  height: 56px;
}
.container {
  max-width: 414px;
  display: flex;
  align-items: center;
  padding: 0 24px;
  margin: 0 auto;
  height: 56px;
}
</style>
