<template>
  <div class= "contactInfo">
    <font-awesome-icon :icon="['fa', iconFontAwesome]"/>
    <h2 class= "contactInfo__title">
      {{titleContact}}
    </h2>
    <p class= "contactInfo__detail">
      {{detailContact}}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    iconFontAwesome: String,
    titleContact: String,
    detailContact: String
  },
  computed: {
    }
  }

</script>

<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';

  .contactInfo {
    @include flexbox(column, center, center);
    line-height: 1.5;
    color: $textColorWhite;
    padding: 0 2vw;

    @include tablet-up {
      width: 20vw;
      height: 30vh;
    }

    svg {
      background-color: $iconColor;
      color: $textColorGreen;
      border-radius: 50%;
      height: 30px;
      width: 30px;
      padding: 3vh;
      margin-bottom: 2vh;
    }

    &__title{
      font-size: 20px;
      font-family: $ralewayMedium;
      

      @include tablet-up {
        font-size: 24px;
      }

    }

    &__detail {
      font-family: $ralewayRegular;
      font-size: 16px;
    }
  }
  
</style>