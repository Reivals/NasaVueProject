<template>
    <div class="heroImage"/>
</template>

<script>
export default {
    name: 'HeroImage',

}
</script>

<style lang="scss" scoped>

.heroImage {
    width: 100%;
    height: 100vh;
    position: fixed;
    top: 0;
    z-index: -1;
    background-image: url('../assets/background.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 80% 0%;
}

</style>
