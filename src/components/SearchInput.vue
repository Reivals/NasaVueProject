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
  padding: 30px 0 0 0;

  input{
    height: 30px;
    border: 0;
    border-bottom: 1px solid black;
    background: none;
    color: white;
    text-align: center;
    
  }
}

</style>
