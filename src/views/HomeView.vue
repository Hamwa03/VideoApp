<script setup>
import VideoButton from "../components/VideoButton.vue";
import DropDownMenu from "../components/DropDownMenu.vue";
</script>

<template>
  <main class="text-center bg-slate-900">
    <h1 class="text-5xl text-white mt-2">VideoApp</h1>
    <div class="p-4 flex justify-center">
      <DropDownMenu />
      <VideoButton buttonText="Ny video" />
    </div>

    <div class="rounded-xl bg-white flex justify-center p-2 mx-8">
      <video class="w-3/4" src=""></video>
    </div>
  </main>
</template>
