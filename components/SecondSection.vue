<template>
  <section id="services" class="secondSection">
    <HeaderSection titleHeader="SERVICE"/>
    <AllServiceCard/>
  </section>
</template>


<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';
  
  .secondSection {
    min-height: 100vh;
    //width: 100vw;
    background-color: $primaryBackgroundColor;
    padding: 0 5vw;

    @include tablet-up {
        @include flexbox( column, space-around, center);
    }

    @include desktop-up {
      padding: 18vw;
    }
  }
</style>