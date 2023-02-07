<script setup>
import VideoButton from "../components/VideoButton.vue";
import DropDownMenu from "../components/DropDownMenu.vue";
</script>

<template>
  <main class="text-center">
    <h1 class="text-2xl text-white">VideoApp</h1>

    <div class="rounded-xl bg-white p-2">
      <DropDownMenu />
      <video class="" src=""></video>
      <VideoButton buttonText="Knapp" />
    </div>
  </main>
</template>
