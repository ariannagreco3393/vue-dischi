<template>
  <header id="site_header">
    <nav class="navbar navbar-light">
      <div class="container-fluid menu">
        <logo />
        <filtri v-model="selectValue" @change="selectGenre"/>
      </div>
    </nav>
  </header>
</template>

<script>
import logo from "@/components/logoComponent.vue";
import filtri from "@/components/filtriComponent.vue";
import state from "@/state";

export default {
  name: "siteHeaderComponent",
  components: {
    logo,
    filtri
  },

  data() {
    return {
      selectValue: '',
    }
    
  },

  methods: {
    selectGenre(){
      state.selectValue = this.selectValue
    }
  }

  
};
</script>

<style lang="scss" scoped>
.navbar {
  height: 60px;
  background-color: #2f3a46;
}
</style>