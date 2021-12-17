<template>
  <div :class="$style.flex">
    <slot v-if="$scopedSlots.default" />
    <slot v-else>
      <div v-for="(item, index) in data" :key="index">
        <o-text align="center" :style="{ fontSize: item.fontSize }"><strong>{{ item.text }}</strong></o-text>
      </div>
    </slot>
  </div>
</template>
<script>
import OText from "./o-text";

export default {
  name: "OFlex",
  components: {
    OText
  },
  props: {
    data: { type: Array, required: false }
  }
}
</script>
<style module>
.flex {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
  overflow: auto;
}

.flex > * {
  max-width: 110px;
  width: 100%;
  flex: 0 0 110px;
  height: 110px;
  margin: 0 auto;

  display: flex;
  justify-content: center;
  align-items: center;

  border-radius: 20px;
  background: linear-gradient(var(--sqr-degrees), var(--sqr-primary), var(--sqr-secondary));
}

.flex > * > * {
  width: 90px;
  margin: 0;
}
</style>
