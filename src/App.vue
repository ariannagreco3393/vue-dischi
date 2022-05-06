<template>
  <div id="app">
    <siteHeader/>
    <!-- /#site_header -->
    <siteMain/>
    <!-- /#site_main -->
  </div>
</template>

<script>
import siteHeader from "@/components/siteHeaderComponent.vue";
import siteMain from "@/components/siteMainComponent.vue";
export default {
  name: 'App',
  components: {
    siteHeader,
    siteMain
  }
}
</script>

<style lang="scss">

</style>
