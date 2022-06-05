<template>
  <input
    class="input"
    type="text"
    :placeholder="placeholderText"
    minlength="3"
    maxlength="20"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    required
  />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TextInput",
  props: ["placeholderText", "modelValue"],
  emits: ["update:modelValue"],
});
</script>

<style scoped lang="scss" src="./TextInput.scss" />
