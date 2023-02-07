<script setup>
import VideoButton from "../components/VideoButton.vue";
import DropDownMenu from "../components/DropDownMenu.vue";
</script>

<template>
  <main class="text-center">
    <h1 class="text-2xl text-white">VideoApp</h1>
    <DropDownMenu />
    <div class="rounded-xl bg-white flex justify-center p-2">
      <video class="w-3/4" src=""></video>
    </div>
  </main>
</template>
