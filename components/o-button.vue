<template>
  <component
    :is="type"
    :class="[
      $style.button,
      color && $style[color],
      roundness && $style[roundness],
      center && $style.center
    ]"
    :style="{ maxWidth: width && width + 'px' }"
    :to="to ? to : null"
    :href="href ? href : null"
  >
    <slot />
  </component>
</template>
<script>
export default {
  name: "OButton",
  computed: {
    type() {
      if ( this.to ) return "nuxt-link"
      else if ( this.href ) return "a"
      return "button"
    },
  },
  props: {
    to: { type: String },
    href: { type: String },
    block: { type: Boolean, default: false },
    color: { type: String },
    roundness: { type: String | Number },
    width: { type: String | Number },
    center: { type: Boolean, default: false },
    loading: { type: Boolean, default: false }
  }
}
</script>
<style module>
.button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: auto;
  height: 42px;
  padding: 0 15px;
  border-radius: 10px;
  border: 1px solid transparent;

  text-decoration: none !important;
  cursor: pointer;
}

/* SIZES */
.block {
  max-width: none !important;
}

/* COLORS */
.green {
  color: var(--color-white);
  background-color: var(--color-secondary);
  border-color: var(--color-secondary);
}

/* ROUNDNESS */
.roundness-sm {
  border-radius: 5px;
}

/* POSITIONS */
.center {
  margin-left: auto;
  margin-right: auto;
}
</style>
