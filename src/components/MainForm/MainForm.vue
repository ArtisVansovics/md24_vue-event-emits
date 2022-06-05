<template>
  <form class="form" v-on:submit.prevent="submitHandler">
    <div class="row"><slot></slot></div>
    <div class="row"><slot name="second-row"></slot></div>
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
