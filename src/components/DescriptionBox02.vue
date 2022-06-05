<template>
  <EventContainer>
    <MainForm>
      <TextInput placeholder-text="Update title..." v-model="inputValueTitle" />
      <template #second-row>
        <TextInput
          placeholder-text="Update description..."
          v-model="inputValueDesc"
        />
      </template>
    </MainForm>
    <TextSquare>
      <p>{{ updatedTitle }}</p>
      <p>{{ updatedDescription }}</p>
    </TextSquare>
  </EventContainer>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import EventContainer from "@/components/EventContainer/EventContainer.vue";
import TextInput from "@/components/TextInput/TextInput.vue";
import MainForm from "@/components/MainForm/MainForm.vue";
import TextSquare from "@/components/TextSquare/TextSquare.vue";

export default defineComponent({
  name: "DescriptionBox02",
  components: { TextSquare, TextInput, MainForm, EventContainer },
  data: () => ({
    inputValueTitle: "",
    inputValueDesc: "",
    title: "Title",
    description: "Description",
  }),
  computed: {
    updatedTitle() {
      if (this.inputValueTitle === "") {
        return this.title;
      } else return this.inputValueTitle;
    },
    updatedDescription() {
      if (this.inputValueDesc === "") {
        return this.description;
      } else return this.inputValueDesc;
    },
  },
});
</script>

<style scoped lang="scss" />
