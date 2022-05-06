<template>
  <div class="col" >
    <div class="wrapper text-center" style="width: 10rem">
      <div class="album">
        <img class="img-fluid" :src="album.poster" alt="" />
      </div>
      <div class="title text-white text-uppercase">
        <h6 class="fw-bold">{{ album.title }}</h6>
      </div>
      <div class="artist">
        <p>
          {{ album.author }} <br />
          {{ album.year }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'listAlbumComponent',
    props: {
        album: Object
    }
}
</script>

<style lang="scss" scoped>
  .col {
      margin: 1rem 0;
    }

  .wrapper {
    padding: 1rem;
    background-color: #2f3a46;
    height: 300px;
    .title {
      margin-top: 1rem;
    }
    .artist {
      color: gray;
      margin-top: 1rem;
      font-size: 14px;
    }
  }
</style>