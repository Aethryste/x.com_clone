<script lang="ts">
import SideNav from "../components/side-nav.vue";

export default {
  name: 'sideNavButton',
  components: {SideNav}
}
</script>

<template>
  <div class="page-wrapper">
    <sideNav/>
  </div>
</template>

<style scoped>
.page-wrapper {
  position: absolute;
  top: 0;
  left: 0;
  width: 100dvw;
  height: 100dvh;
}
</style>