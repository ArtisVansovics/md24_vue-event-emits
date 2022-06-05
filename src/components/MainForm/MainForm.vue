<template>
  <form class="form" v-on:submit.prevent="submitHandler">
    <slot></slot>
  </form>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "MainForm",
  emits: ["onSubmit"],
  methods: {
    submitHandler() {
      this.$emit("onSubmit");
    },
  },
});
</script>

<style scoped lang="scss" src="./MainForm.scss" />
