<template>
  <EventContainer>
    <MainForm>
      <TextInput placeholder-text="Update title..." v-model="inputValueTitle" />
      <MainButton :onClick="updateTitle" :is-disabled="titleSubmitDisabled">
        Change
      </MainButton>
      <template #second-row>
        <TextInput
          placeholder-text="Update description..."
          v-model="inputValueDesc"
        />
        <MainButton
          :onClick="updateDescription"
          :is-disabled="descSubmitDisabled"
        >
          Change
        </MainButton>
      </template>
    </MainForm>
    <TextSquare>
      <p>{{ currentTitle }}</p>
      <p>{{ currentDescription }}</p>
    </TextSquare>
  </EventContainer>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import EventContainer from "@/components/EventContainer/EventContainer.vue";
import MainButton from "@/components/MainButton/MainButton.vue";
import TextInput from "@/components/TextInput/TextInput.vue";
import MainForm from "@/components/MainForm/MainForm.vue";
import TextSquare from "@/components/TextSquare/TextSquare.vue";

export default defineComponent({
  name: "DescriptionBox01",
  components: { TextSquare, MainButton, TextInput, MainForm, EventContainer },
  data: () => ({
    inputValueTitle: "",
    inputValueDesc: "",
    currentTitle: "Title",
    currentDescription: "Description",
  }),
  computed: {
    titleSubmitDisabled() {
      return this.inputValueTitle.length < 4;
    },
    descSubmitDisabled() {
      return this.inputValueDesc.length < 4;
    },
  },
  methods: {
    updateTitle() {
      this.currentTitle = this.inputValueTitle;

      this.inputValueTitle = "";
    },
    updateDescription() {
      this.currentDescription = this.inputValueDesc;

      this.inputValueDesc = "";
    },
  },
});
</script>

<style scoped lang="scss" />
