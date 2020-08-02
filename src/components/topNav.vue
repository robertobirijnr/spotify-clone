<template>
  <div class="w-full h-full relative">
    <div class="w-full sticky top-0 py-4 px-6 flex item-center justify-between">
      <div class="flex item-center">
        <button class="rounded-full bg-black w-8 h8 text-white mr-3">
          <i class="material-icons">navigate_before</i>
        </button>
        <button class="rounded-full bg-black w-8 h8 text-white">
          <i class="material-icons">navigate_next</i>
        </button>
      </div>
      <div class="relative">
        <button
          @click="showdropdown = true"
          class="focus:outline-none bg-black rounded-full py-1 px-2 flex items-center"
        >
          <p class="text-white font-semibold text-xs mr-3">Robert Obiri Jnr</p>
          <i v-if="showdropdown === false" class="material-icons text-white"
            >arrow_drop_down</i
          >
          <i v-if="showdropdown === true" class="material-icons text-white"
            >arrow_drop_up</i
          >
        </button>
        <div
          v-if="showdropdown === true"
          class="absolute bg-gray-800 w-full rounded mt-1"
        >
          <button
            @click="showdropdown = false"
            class="focus:outline-none w-full text-sm py-2 text-gray-600 hover:text-white border-b border-white opacity-75 hover:opacity-100"
          >
            Register
          </button>
          <button
            @click="showdropdown = false"
            class="focus:outline-none w-full text-sm py-2 text-gray-600 hover:text-white"
          >
            Login
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showdropdown: false,
    };
  },
};
</script>
