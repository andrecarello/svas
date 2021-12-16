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
  display: flex;
  justify-content: flex-start;
  align-items: stretch;
  gap: 18px;
  overflow: auto;
}

.flex > * {
  max-width: 110px;
  width: 100%;
  flex: 0 0 110px;
  height: 110px;

  display: flex;
  justify-content: center;
  align-items: center;

  border-radius: 20px;
  background: linear-gradient(var(--color-blue-500), var(--color-blue-800));
}

.flex > * > * {
  width: 90px;
  margin: 0;
}
</style>
