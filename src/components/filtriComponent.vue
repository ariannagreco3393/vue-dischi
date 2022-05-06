<template>
  <div class="filtri">
    <select
      name="genre"
      id="genre"
      :value="selectValue"
      @input="$emit('input', $event.target.value)"
      @change="$emit('selectGenre')"
    >
      <option>All</option>
      <option>Rock</option>
      <option>Pop</option>
      <option>Jazz</option>
      <option>Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "filtriComponent",
  props: {
    selectValue: String,
  },
};
</script>

<style lang="scss" scoped>
.filtri {
  select {
    border: none;
    padding: 0.3rem;
    font-size: 14px;
    background-color: #18d860;
    color: black;
    font-weight: 500;
    border-radius: 10px;
  }
}
</style>