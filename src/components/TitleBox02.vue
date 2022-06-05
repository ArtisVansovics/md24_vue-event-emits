<template>
  <EventContainer>
    <template #header>
      <h2>
        {{ updatedTitle }}
      </h2>
    </template>
    <MainForm>
      <TextInput placeholder-text="Update title..." v-model.lazy="inputValue" />
    </MainForm>
  </EventContainer>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import EventContainer from "@/components/EventContainer/EventContainer.vue";
import TextInput from "@/components/TextInput/TextInput.vue";
import MainForm from "@/components/MainForm/MainForm.vue";

export default defineComponent({
  name: "TitleBox02",
  components: { TextInput, MainForm, EventContainer },
  data: () => ({
    inputValue: "",
    title: "Title",
  }),
  computed: {
    updatedTitle() {
      if (this.inputValue === "") {
        return this.title;
      } else return this.inputValue;
    },
  },
});
</script>

<style scoped lang="scss" />
