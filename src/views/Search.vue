<template>
  <div class="searchWrapper">
      <Claim/>
      <SearchInput/>
  </div>
</template>

<script>
import Claim from '@/components/Claim.vue'
import SearchInput from '@/components/SearchInput.vue'
export default {
  name: 'Search',
  components: {
    Claim,
    SearchInput,
  },
  data() {
    return {
        searchValue: '',
    };
  },
  methods: {
    handleInput(e){
      console.log(this.searchValue);
    },
  }
};
</script>
<style lang="scss" scoped>

.searchWrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0;
  padding: 30px;
  width: 100%;
  background-image: url('../assets/background.jpg');
  height: 100vh;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 80% 0%;
  justify-content: center;
}



</style>
