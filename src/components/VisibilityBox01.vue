<template>
  <EventContainer>
    <MainForm :onSubmit="toggleVisibility">
      <p>Toggle square visibility on button click.</p>
      <template #second-row>
        <MainButton>Toggle</MainButton>
      </template>
    </MainForm>
    <AdjustableSquare v-if="squareVisibility" />
  </EventContainer>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import EventContainer from "@/components/EventContainer/EventContainer.vue";
import MainButton from "@/components/MainButton/MainButton.vue";
import MainForm from "@/components/MainForm/MainForm.vue";
import AdjustableSquare from "@/components/AdjustableSquare/AdjustableSquare.vue";

export default defineComponent({
  name: "VisibilityBox01",
  components: {
    MainButton,
    MainForm,
    EventContainer,
    AdjustableSquare,
  },
  data: () => ({
    squareVisibility: true,
  }),
  methods: {
    toggleVisibility() {
      this.squareVisibility = !this.squareVisibility;
    },
  },
});
</script>

<style scoped lang="scss" />
