<template>
  <div class="square">
    <slot></slot>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TextSquare",
});
</script>

<style scoped lang="scss" src="./TextSquare.scss" />
