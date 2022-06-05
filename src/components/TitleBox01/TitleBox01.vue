<template>
  <EventContainer>
    <template #header
      ><h2>{{ currentTitle }}</h2></template
    >
    <MainForm :onSubmit="updateTitle">
      <TextInput placeholder-text="Update title..." v-model="inputValue" />
      <MainButton>Submit</MainButton>
    </MainForm>
  </EventContainer>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import EventContainer from "@/components/EventContainer/EventContainer.vue";
import MainButton from "@/components/MainButton/MainButton.vue";
import TextInput from "@/components/TextInput/TextInput.vue";
import MainForm from "@/components/MainForm/MainForm.vue";

export default defineComponent({
  name: "TitleBox01",
  components: { MainButton, TextInput, MainForm, EventContainer },
  data: () => ({
    inputValue: "",
    currentTitle: "Title",
  }),
  methods: {
    test() {
      console.log("check");
    },
    updateTitle() {
      this.currentTitle = this.inputValue;

      this.inputValue = "";
    },
  },
});
</script>

<style scoped lang="scss" />
