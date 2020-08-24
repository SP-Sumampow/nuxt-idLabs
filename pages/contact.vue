<template>
  <div class="contactPage">
    <HeaderSection titleHeader="CONTACT"/>
    <AllContact/>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';

  .contactPage {
    max-width: 100vw;
    height: 100vh;
    background-color: $secondaryBackgroundColor;
    @include flexbox(column, center, center);
    padding: 0 5vw;

    @include desktop-up {
      padding: auto 20vw;
    }
  }
  
</style>