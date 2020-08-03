<template>
  <div class="flex" style="height:90vh">
    <div class="w-56 bg-black h-full flex-none">
      <div class="p-6">
        <img src="../assets/logo-01.png" alt />
      </div>
      <div class="mx-2 mb-5">
        <button
          v-for="page in pages"
          :key="page.id"
          @click="setID = page.id"
          :class="
            `w-full text-sm font-semibold focus:outline-none rounded text-white px-3 py-2 flex items-cnter justify-start ${
              setID === page.id ? 'bg-teal-300 text-white' : 'bg-yellow'
            }`
          "
        >
          <i class="material-icons mr-3">{{ page.icon }}</i>
          <p>{{ page.name }}</p>
        </button>
      </div>
      <div class="mx-5">
        <h1 class="text-xs mb-3 text-white tracking-widest uppercase">Playlists</h1>
        <button class="flex text-white justify-start item-center opacity-75 hover:opacity-100 mb-2">
          <div></div>
          <i class="material-icons mr-3">create_new_folder</i>
          <p class="text-white text-sm font-semibold">Create Playlist</p>
        </button>
        <button class="flex text-white justify-start item-center opacity-75 hover:opacity-100">
          <div></div>
          <i class="material-icons mr-3">stars</i>
          <p class="text-white text-sm font-semibold">Liked Songs</p>
        </button>
        <div class="h-px w-full bg-white my-3"></div>
      </div>
      <div class="mx-5 pb-3">
        <div class="w-full h-24 overflow-y-scroll">
          <p
            v-for="album in albums"
            :key="album.name"
            class="text-white hover:text-teal text-sm py-1"
          >{{ album.name }}</p>
        </div>
      </div>
      <div class="mx-5 pb-3">
        <button class="flex text-white justify-start item-center opacity-75 hover:opacity-100">
          <div></div>
          <i class="material-icons mr-3">cloud_download</i>
          <p class="text-white text-sm font-semibold">Install App</p>
        </button>
      </div>
      <div class="relative pb-3">
        <img src />
      </div>
    </div>
    <TopNav />
  </div>
</template>

<script>
import TopNav from "@/components/topNav.vue";
export default {
  components: {
    TopNav,
  },
  data() {
    return {
      pages: [
        { id: "home", name: "Home", icon: "home" },
        { id: "search", name: "Search", icon: "search" },
        { id: "Library", name: "Your Libray", icon: "bar_chart" },
      ],
      setID: "search",
      albums: [
        { name: "cheese" },
        { name: "shybreseafo" },
        { name: "Marry" },
        { name: "obiato" },
        { name: "Anloga" },
        { name: "Kwame Nkrumah" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
