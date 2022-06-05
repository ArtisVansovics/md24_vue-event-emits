<template>
  <input :class="['checkbox', { checked: isChecked }]" type="checkbox" />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "CustomCheckbox",
  props: ["isChecked"],
});
</script>

<style scoped lang="scss" src="./CustomCheckbox.scss" />
