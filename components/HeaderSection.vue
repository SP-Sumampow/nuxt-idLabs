<template>
  <div class= "titleSection">
    <h2 class= "titleSection__text">
      {{titleHeader}}
    </h2>
    <p v-if="hasSubTitleHeader" class= "titleSection___subText">
      {{subTitleHeader}}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    titleHeader: String,
    subTitleHeader: String
  },
  computed: {
    hasSubTitleHeader: function () {
      return this.subTitleHeader !== undefined
    }
  }
}
</script>

<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';

  .titleSection {
    align-self: flex-start;
    font-family: $poppinsBold;
    font-size: 50px;
    color: $textColorGreen;
    line-height: 1.5;

     &___subText {
      font-size: 16px;
      font-family: $ralewayRegular;
      color: $textColorWhite;

      @include tablet-up {
        font-size: 20px;
      }

    }
  }
  
</style>