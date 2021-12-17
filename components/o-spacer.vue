<template>
  <div :style="{
    height: '1px',
    width: '1px',
    marginTop: this.top && this.size(this.top),
    marginBottom: this.bottom && this.size(this.bottom),
    marginLeft: this.left && this.size(this.left)
  }" />
</template>
<script>
export default {
  name: "OSpacer",
  props: {
    top: { type: String },
    left: { type: String },
    bottom: { type: String },
  },
  methods: {
    size(value) {
      return value === "auto" ? "auto" : (value - 1)+"px"
    }
  },
}
</script>
