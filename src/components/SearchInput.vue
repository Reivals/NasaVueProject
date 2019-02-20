<template>
    <div class="searchInputWrapper">
      <input 
      name="search" 
      id="search" 
      :value="value"
      @input="handleChange"
      />
    </div>
</template>

<script>
export default {
    name: "SearchInput",
    props: {
      value: {
        type: String,
        required: true,
      },
    },
    methods: {
      handleChange(e){
        this.$emit('input', e.target.value);
      },
    }
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
