<template>
  <div class="app">
    <div class="container">
      <div class="column">
        <TitleBox01 />
        <TitleBox02 />
      </div>
      <div class="column"></div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TitleBox01 from "@/components/TitleBox01.vue";
import TitleBox02 from "@/components/TitleBox02.vue";

export default defineComponent({
  name: "App",
  components: { TitleBox01, TitleBox02 },
});
</script>

<style scoped lang="scss" src="./styles/App.scss" />
