<template>
  <component
    :is="tag"
    :class="[
      $style.text,
      $style[color],
      $style[align],
      size && $style[size]
    ]"
    :style="setWidth"
  ><slot /></component>
</template>
<script>
export default {
  name: "OText",
  props: {
    tag: { type: String, default: "p" },
    size: { type: String },
    color: { type: String, default: "white" },
    align: { type: String, default: "left" },
    width: { type: String }
  },
  computed: {
    setWidth() {
      if (!this.width) return;

      let e = this.width === 'auto' ? '100%' : this.width+'px';
      return `maxWidth: ${ e }; margin-left: auto; margin-right: auto`;
    }
  }
}
</script>
<style module>
.text {
  font-size: 14px;
  line-height: 1.21;
  margin-bottom: 17px;
}

strong {
  font-weight: 900;
}

/* COLORS */
.white { color: var(--color-white); }
.green { color: var(--color-secondary); }
.blue { color: var(--color-blue-800); }

/* ALIGNMENT */
.center { text-align: center }
.left { text-align: left }
.right { text-align: right}
.justfy { text-align: justify }

/* SIZES */
.large { font-size: 16px; line-height: 20px; }
strong {
  font-weight: bold;
}
</style>
