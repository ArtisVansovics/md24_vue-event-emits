<template>
  <EventContainer>
    <MainForm :onSubmit="updateColor">
      <TextInput placeholder-text="Change color..." v-model="inputValue" />
      <MainButton>Change</MainButton>
    </MainForm>
    <AdjustableSquare :current-color="currentColor" />
  </EventContainer>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import EventContainer from "@/components/EventContainer/EventContainer.vue";
import MainButton from "@/components/MainButton/MainButton.vue";
import TextInput from "@/components/TextInput/TextInput.vue";
import MainForm from "@/components/MainForm/MainForm.vue";
import AdjustableSquare from "@/components/AdjustableSquare/AdjustableSquare.vue";

export default defineComponent({
  name: "ColorBox01",
  components: {
    MainButton,
    TextInput,
    MainForm,
    EventContainer,
    AdjustableSquare,
  },
  data: () => ({
    inputValue: "",
    currentColor: "",
  }),
  methods: {
    updateColor() {
      this.currentColor = this.inputValue;

      this.inputValue = "";
    },
  },
});
</script>

<style scoped lang="scss" />
