<template>
  <div class="appWrapper">
      <Claim/>
      <SearchInput/>
      <HeroImage/>
  </div>
</template>

<script>
import HeroImage from '@/components/HeroImage.vue'
import Claim from '@/components/Claim.vue'
import SearchInput from '@/components/SearchInput.vue'
export default {
    name: "App",
    components: {
      Claim,
      SearchInput,
      HeroImage,
    }
}
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
