<template>
  <EventContainer>
    <MainForm>
      <TextInput placeholder-text="Change color..." v-model="inputValue" />
    </MainForm>
    <AdjustableSquare :current-color="updatedColor" />
  </EventContainer>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import EventContainer from "@/components/EventContainer/EventContainer.vue";
import TextInput from "@/components/TextInput/TextInput.vue";
import MainForm from "@/components/MainForm/MainForm.vue";
import AdjustableSquare from "@/components/AdjustableSquare/AdjustableSquare.vue";

export default defineComponent({
  name: "ColorBox02",
  components: {
    TextInput,
    MainForm,
    EventContainer,
    AdjustableSquare,
  },
  data: () => ({
    inputValue: "",
  }),
  computed: {
    updatedColor() {
      return this.inputValue;
    },
  },
});
</script>

<style scoped lang="scss" />
