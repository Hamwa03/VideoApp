<script setup>
import VideoButton from "../components/VideoButton.vue";
import DropDownMenu from "../components/DropDownMenu.vue";
</script>

<template>
  <main class="text-center">
    <h1 class="text-5xl text-white mt-2">VideoApp</h1>
    <DropDownMenu />
    <VideoButton buttonText="Ny video" />

    <div class="rounded-xl bg-white flex justify-center p-2 mx-8 mt-4">
      <video class="w-3/4" src=""></video>
    </div>
  </main>
</template>
