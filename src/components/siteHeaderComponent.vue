<template>
  <header id="site_header">
    <nav class="navbar navbar-light">
      <div class="container-fluid menu">
          <logo/>
      </div>
    </nav>
  </header>
</template>

<script>
import logo from '@/components/logoComponent.vue'
export default {
  name: "siteHeaderComponent",
  components: {
      logo
  }
};
</script>

<style lang="scss" scoped>
.navbar {
    height: 60px;
    background-color: #2f3a46;
}
</style>