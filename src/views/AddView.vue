<template>
  <main class="text-center">
    <h1 class="text-2xl text-white">Add Video</h1>
    <div class="rounded-xl bg-white flex justify-center p-2">
      <input placeholder="Video link" class="rounded border-2" />

      <VideoButton buttonText="Add video" class="" />
    </div>
  </main>
</template>

<script setup>
import VideoButton from "../components/VideoButton.vue";
</script>
