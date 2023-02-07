<template>
  <main class="text-center bg-slate-900">
    <h1 class="text-5xl text-white mt-2">VideoApp</h1>
    <div class="p-4 flex justify-center">
      <DropDownMenu :videos="videos" />
      <VideoButton buttonText="Ny video" @click="addVideo" />
      <input type="text" v-model="newUrl" />
    </div>

    <div class="rounded-xl bg-white flex justify-center p-2 mx-8">
      <video class="w-3/4" src=""></video>
    </div>
  </main>
</template>

<script>
import VideoButton from "../components/VideoButton.vue";
import DropDownMenu from "../components/DropDownMenu.vue";

export default {
  components: {
    VideoButton,
    DropDownMenu,
  },
  data() {
    return {
      videos: [],
      newUrl: "",
    };
  },
  methods: {
    getVideo() {
      const XHR = new XMLHttpRequest();
      const view = this;
      XHR.onload = function () {
        view.videos = JSON.parse(this.responseText).videos;
      };
      XHR.open("GET", "https://videoserver-db59.onrender.com/videos");
      XHR.send();
    },
    addVideo() {
      const XHR = new XMLHttpRequest();
      const view = this;
      const newVideo = { url: view.newUrl };
      view.newUrl = "";
      XHR.onload = function () {
        view.videos.push(newVideo);
      };
      XHR.open("POST", "https://videoserver-db59.onrender.com/videos");
      XHR.setRequestHeader("Content-type", "application/json");
      XHR.send(JSON.stringify(newVideo));
    },
  },
  mounted() {
    this.getVideo();
    console.log("test");
  },
};
</script>
