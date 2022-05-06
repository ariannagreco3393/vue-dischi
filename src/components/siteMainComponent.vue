<template>
  <main id="site_main">
    <album/>
  </main>
</template>

<script>
import album from "@/components/albumComponent.vue"
export default {
  name: "siteMainComponent",
  components: {
      album
  },
 
};
</script>

<style lang="scss" scoped>
#site_main {
  height: calc(100vh - 60px);
  background-color: #1e2d3b;
}
</style>