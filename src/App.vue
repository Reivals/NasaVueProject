<template>
  <div class="appWrapper">
      <Claim/>
      <SearchInput v-model="searchValue" @input="handleInput"/>
      <HeroImage/>
  </div>
</template>

<script>
import HeroImage from '@/components/HeroImage.vue'
import Claim from '@/components/Claim.vue'
import SearchInput from '@/components/SearchInput.vue'
import debounce from 'lodash.debounce'
const axios = require('axios');
const API = 'https://images-api.nasa.gov/search';
export default {
    name: "App",
    components: {
      Claim,
      SearchInput,
      HeroImage,
    },
    data() {
      return {
        searchValue : '',
        results: [],
      }
    },
    methods : {
      handleInput: debounce(function(){
      axios.get(`${API}?q=${this.searchValue}&media_type=image`)
      .then((response) => {
        console.log(response);
        this.results = response.data.collection.items;
      })
      },500),

    },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Montserrat');
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
  margin: 0;
  padding: 0;
}

.appWrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0;
  padding: 30px;
  width: 100%;
  height: 100vh;
  justify-content: center;
}



</style>
