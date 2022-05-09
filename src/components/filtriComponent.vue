<template>
  <select
    name="genre"
    id="genre"
    :value="selectValue"
    @change=""
  >
    <option value="">Seleziona un genere</option>
    <option :value="genre" v-for="(genre, index) in getGenres" :key="index">Rock</option>
  </select>
</template>

<script>
export default {
  name: "filtriComponent",
  props: {
    value: String,
  },
};
</script>

<style lang="scss" scoped>
select {
  border: none;
  padding: 0.3rem;
  font-size: 14px;
  background-color: #18d860;
  color: black;
  font-weight: 500;
  border-radius: 10px;
}
</style>