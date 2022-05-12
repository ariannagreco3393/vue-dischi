<template>
  <header id="site_header">
    <nav class="navbar navbar-light">
      <div class="container-fluid menu">
        <logo />
        <select
          v-model="selectValue"
          @change="selectGenre"
          name="genre"
          id="genre"
        >
          <option value="">Seleziona un genere</option>
          <option
            :value="genre"
            v-for="(genre, index) in getGenres"
            :key="index"
          >
            {{ genre }}
          </option>
        </select>
        
      </div>
    </nav>
  </header>
</template>

<script>
import logo from "@/components/logoComponent.vue";
import state from "@/state";

export default {
  name: "siteHeaderComponent",
  components: {
    logo,
  },

  data() {
    return {
      selectValue: "",
    };
  },
  computed: {
    getGenres() {
      return state.genres;
    },
  },

  methods: {
    selectGenre() {
      state.selectValue = this.selectValue;
    },
  },
};
</script>

<style lang="scss" scoped>
.navbar {
  height: 60px;
  background-color: #2f3a46;
}
</style>