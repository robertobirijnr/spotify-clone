<template>
  <div class="bg-gray-900 h-screen">
    <sidenav/>
    <div class="w-full bg-gray-800" style="height:10vh"></div>
  </div>
</template>

<script>
// @ is an alias to /src
import sidenav from '@/components/sideNav.vue'

export default {
  name: "Home",
  components:{
    sidenav,
  }
};
</script>
