<template>
  <div class="app">
    <div class="container">
      <TitleBox01 />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TitleBox01 from "@/components/TitleBox01/TitleBox01.vue";

export default defineComponent({
  name: "App",
  components: { TitleBox01 },
});
</script>

<style scoped lang="scss" src="./styles/App.scss" />
