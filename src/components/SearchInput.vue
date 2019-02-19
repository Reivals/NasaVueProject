<template>
    <div class="searchInputWrapper">
      <input name="search" 
      id="search" 
      v-model="searchValue" 
      @input="handleInput"/>
    </div>
</template>

<script>
export default {
    name: "SearchInput",
}
</script>

<style lang="scss" scoped>
.searchInputWrapper {
  width: 250px;
  display: flex;
  flex-direction: column;

  input{
    height: 30px;
    border: 0;
    border-bottom: 1px solid black;
    background: none;
  }
}

</style>
