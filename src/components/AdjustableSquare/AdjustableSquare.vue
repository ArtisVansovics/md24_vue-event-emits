<template>
  <div class="square" :style="{ backgroundColor: currentColor }" />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "AdjustableSquare",
  props: ["currentColor"],
});
</script>

<style scoped lang="scss" src="./AdjustableSquare.scss" />
