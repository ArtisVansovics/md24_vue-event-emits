<template>
  <div class="event-container">
    <slot name="header"></slot>
    <div class="row">
      <slot></slot>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "EventContainer",
});
</script>

<style scoped lang="scss" src="./EventContainer.scss" />
