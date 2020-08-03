<template>
  <div class="bg-gray-900 h-screen">
    <sidenav />
    <div class="w-full bg-gray-800 flex items-center justify-between px-3" style="height:10vh">
      <div class="flex items-center">
        <div>
          <h1 class="text-sm text-white tracking-wide">wagye me - Obaapa Christy</h1>
          <h2 class="text-xs text-teal-600 tracking-wide">Hyebre Sesafo</h2>
        </div>
        <i class="material-icons text-xl text-green-600 mx-4">favorite</i>
        <i class="material-icons text-xl text-gray-400">picture_in_picture_alt</i>
      </div>
      <div class="flex flex-col justify-center w-1/2 items-center">
        <div class="flex items-center">
          <button class="text-lg text-gray-700 hover:text-white">
            <i class="material-icons">shuffle</i>
          </button>
          <button class="text-lg text-gray-700 hover:text-white">
            <i class="material-icons">skip_previous</i>
          </button>
          <button class="h-8 w-8 text-gray-700 hover:text-white">
            <i class="material-icons">play_circle_outline</i>
          </button>
          <button class="text-lg text-gray-700 hover:text-white">
            <i class="material-icons">skip_next</i>
          </button>
          <button class="text-lg text-gray-700 hover:text-white">
            <i class="material-icons">repeat</i>
          </button>
        </div>

        <div class="w-full">
          <div class="w-full h-1 bg-black rounded-full mt-4 flex items-center">
            <div class="h-1 rounded-full bg-green-600" style="width: 18%"></div>
            <div class="h-3 w-3 bg-white rounded-full -ml-1 shadow"></div>
          </div>
        </div>
      </div>
      <div class="flex items-center">
        <i class="material-icons text text-gray-700">playlist_play</i>
        <i class="material-icons text-xl text-gray-700">important_devices</i>
        <i class="material-icons text-xl text-gray-700">volume_up</i>
        <div class="w-20 ml-1 bg-gray-700 rounded-full h-1"></div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import sidenav from "@/components/sideNav.vue";

export default {
  name: "Home",
  components: {
    sidenav,
  },
};
</script>
