<template>
  <EventContainer>
    <MainForm>
      <p>Toggle square visibility on checkbox click.</p>
      <template #second-row>
        <CustomCheckbox
          :is-checked="squareVisibility"
          :onchange="toggleVisibility"
        />
      </template>
    </MainForm>
    <AdjustableSquare v-if="squareVisibility" />
  </EventContainer>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import EventContainer from "@/components/EventContainer/EventContainer.vue";
import MainForm from "@/components/MainForm/MainForm.vue";
import AdjustableSquare from "@/components/AdjustableSquare/AdjustableSquare.vue";
import CustomCheckbox from "@/components/CustomCheckbox/CustomCheckbox.vue";

export default defineComponent({
  name: "VisibilityBox02",
  components: {
    CustomCheckbox,
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
