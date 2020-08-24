<template>
  <div class= "progression">
    <div class= "progression__text progressionText">
      <h3 class= "progressionText__title">
        {{title}}
      </h3>
      <h3 class= "progressionText__number">
        {{`${this.percent}%`}}
      </h3>
    </div>
    <diV class="progression__bar">
      <transition name="fillBarProgrees">
        <span class="barProgrees" :style="{ width: percentDisplay + '%' }"></span>
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    percent: Number,
    shouldBeDisplay: Boolean
  },
  created: function () {},
  computed: {
    percentDisplay: function () {
      return this.shouldBeDisplay ? this.percent : 0
    }
  }
}
</script>

<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';

  .progression {
    font-family: $ralewayRegular;
    font-size: 18px;
    color: $textColorWhite;
    line-height: 1.5;
    margin-bottom: 2vh;
    //width: 90vw;

    // @include desktop-up {
    //   width: ;
    // }

    &__text {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      font-size: 18px;
      color: $textColorWhite;
      margin-bottom: 1vh;
    }

    &__bar {
      width: 100%;
      height: 16px;
      background-color: $iconColor;

      .barProgrees {
        //display: block;
        height: 100%;
        display: block;
        background-color: $textColorGreen;
        transition: width 3s ease 0s;
      }
    }

    //border: 1px solid white;

  }
  
</style>