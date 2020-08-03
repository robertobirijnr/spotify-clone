<template>
  <div>
    <div class="px-6 py-3">
      <div class="flex items-center justify-between">
        <h1
          class="pl-2 text-2xl font-semibold text-white tracking-wider hover:underline"
        >Recently Played</h1>
        <h2
          class="pr-8 pt-4 text-xs text-white uppercase tracking-wider hover:underline mb-3"
        >See All</h2>
      </div>
      <div class="w-full flex flex-wrap">
        <div v-for="recent in recents" :key="recent.title" class="p-2 w-48 relative">
          <div
            class="absolute w-full h-full flex items-end justify-end p-8 opacity-75 hover:opacity-100"
          >
            <div class="bg-teal-500 rounded-full h-10 w-10 flex items-center justify-center">
              <i class="material-icons text-white text-2xl">play_arrow</i>
            </div>
          </div>
          <div class="bg-gray-600 w-full h-auto p-5 rounded-lg shadow-ad">
            <img :src="`${recent.url}`" class="h-auto w-full shadow mb-2" />
            <h1 class="text-sm font-semibold text-white tracking-wide">{{recent.title}}</h1>
            <h2 class="text-sm text-white tracking-wide pb-5">{{recent.artist}}</h2>
          </div>
        </div>
      </div>
    </div>
    <div class="px-6 py-3">
      <div class="flex items-center justify-between">
        <div class="pl-2">
          <h1
            class="text-2xl font-semibold text-white tracking-wider hover:underline"
          >Special Albums for you</h1>
          <h2 class="text-sm text-teal-500">Get Better Recommendations the more you listen</h2>
        </div>

        <h2
          class="pr-8 pt-4 text-xs text-white uppercase tracking-wider hover:underline mb-3"
        >See All</h2>
      </div>
      <div class="w-full flex flex-wrap">
        <div v-for="spec in special" :key="spec.title" class="p-2 w-48 relative">
          <div
            class="absolute w-full h-full flex items-end justify-end p-8 opacity-75 hover:opacity-100"
          >
            <div class="bg-teal-500 rounded-full h-10 w-10 flex items-center justify-center">
              <i class="material-icons text-white text-2xl">play_arrow</i>
            </div>
          </div>
          <div class="bg-gray-600 w-full h-auto p-5 rounded-lg shadow-ad">
            <img :src="`${spec.url}`" class="h-auto w-full shadow mb-2" />
            <h1 class="text-sm font-semibold text-white tracking-wide">{{spec.title}}</h1>
            <h2 class="text-sm text-white tracking-wide pb-5">{{spec.artist}}</h2>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      recents: [
        {
          url: "anlogo-junction.jpg",
          title: "Angloga Junction",
          artist: "Stoneboy",
        },
        {
          url: "joe-metle.jpg",
          title: "God is coming soon",
          artist: "Joe Metle",
        },
        {
          url: "mary_album.jpg",
          title: "Mary",
          artist: "Sarkodie",
        },
        {
          url: "Yaw-Sarpong-and-the-Asomafo.jpg",
          title: "Asomafo",
          artist: "Yaw Sarpong",
        },
        {
          url: "mdk.jpg",
          title: "Omo Ada",
          artist: "Medikal",
        },
        {
          url: "wagye_me.jpg",
          title: "wagye me",
          artist: "Obaapa Christy",
        },
      ],
      special: [
        {
          url: "sarkology.jpg",
          title: "Highest",
          artist: "Sarkodie",
        },
        {
          url: "revival-worship.jpg",
          title: "Revival song",
          artist: "Joe Metle",
        },
        {
          url: "nkrumah.jpg",
          title: "Nkrumah",
          artist: "Kwesi Arthur",
        },
        {
          url: "kwame_eugen.jpg",
          title: "Rock Star",
          artist: "kwame Eugen",
        },
        {
          url: "mdk.jpg",
          title: "Omo Ada",
          artist: "Medikal",
        },
        {
          url: "kwesi-Arthur-album.jpg",
          title: "Back to Back",
          artist: "Kwesi Arthur",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
