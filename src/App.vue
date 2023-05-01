<script setup>
import ImageGallery from "./components/ImageGallery.vue";
import SideBar from "./components/SideBar.vue";
import { ref } from "vue";
const isWhitColor = ref(true);
const OnClickOption = (isColor) => {
  isWhitColor.value = isColor;
};
</script>

<template>
  <v-app>
    <SideBar @selectOption="OnClickOption"></SideBar>
    <v-main>
      <ImageGallery :isWhiteColor="isWhitColor" />
    </v-main>
  </v-app>
</template>

<style></style>
