<template>
    <section v-if="!loading">
      <div class="container">
        <div class="row">
          <listAlbum :album="album" v-for="(album, index) in albums" :key="index"/>
        </div>
      </div>
    </section>
    <div v-else class="d-flex justify-content-center align-item-center text-info">
        <h1>Loading...</h1>
    </div>
</template>

<script>
import axios from "axios";
import listAlbum from "@/components/listAlbumComponent.vue";

export default {
    name: 'albumComponent',
    components: {
        listAlbum
    },
     data() {
    return {
      API_URL: "https://flynn.boolean.careers/exercises/api/array/music",
      albums: null,
      loading: true,
      error: null,
    };
  },
  methods: {
    callApi() {
      axios
        .get(this.API_URL)
        .then((response) => {
          this.albums = response.data.response;
          this.loading = false;
        })
        .catch((error) => {
          console.error(error);
          this.error = `Sorry There is a problem! ${error}`;
        });
    },
  },
  mounted() {
    this.callApi();
  },
}
</script>

<style lang="scss" scoped>

  .container {
    max-width: 1000px;
  }


</style>