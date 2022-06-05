<template>
  <div class="app">
    <div class="container">
      <div class="column">
        <TitleBox01 />
        <TitleBox02 />
        <ColorBox01 />
        <ColorBox02 />
      </div>
      <div class="column">
        <DescriptionBox01 />
        <DescriptionBox02 />
        <VisibilityBox01 />
        <VisibilityBox02 />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TitleBox01 from "@/components/TitleBox01.vue";
import TitleBox02 from "@/components/TitleBox02.vue";
import ColorBox01 from "@/components/ColorBox01.vue";
import ColorBox02 from "@/components/ColorBox02.vue";
import DescriptionBox01 from "@/components/DescriptionBox01.vue";
import DescriptionBox02 from "@/components/DescriptionBox02.vue";
import VisibilityBox01 from "@/components/VisibilityBox01.vue";
import VisibilityBox02 from "@/components/VisibilityBox02.vue";

export default defineComponent({
  name: "App",
  components: {
    VisibilityBox02,
    VisibilityBox01,
    DescriptionBox02,
    DescriptionBox01,
    ColorBox02,
    ColorBox01,
    TitleBox02,
    TitleBox01,
  },
});
</script>

<style scoped lang="scss" src="./styles/App.scss" />
