<template>
  <div class= "serviceCard">
    <font-awesome-icon :icon="['fa', 'archive']"/>
    <h3 class= "serviceCard__title">
      API REST & GraphQL
    </h3>
    <p class= "serviceCard__text">
      De la stratégie à l’exécution, le succès
      d’une démarche orientée API demande une palette
      très diversifiée de savoir-faire.
    </p>
  </div>
</template>


<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';

  
  .serviceCard {
    max-width: 80vw;
    height: 50vh;
    @include flexbox( column, space-evenly, flex-start);
    margin: 4vh 0 auto auto;
    padding: 5vh 10vw;
    background-color: $secondaryBackgroundColor;
    line-height: 1.5;

    @include tablet-up {
      max-width: 20vw;
      height: 30vh;
      margin: 4vh 0 1vw 1vw;
    }

    @include desktop-up {
      max-width: 15vw;
      height: 25vh;
      margin: 4vh 0 1vw 1vw;
      padding: 2vw;
    }

    .fa-archive {
      color: $iconColor;
      height: 80px;
      width: 80px;
    }

    &__title {
      font-family: $poppinsRegular;
      color: $textColorGreen;
      font-size: 26px;

    }

    &__text {
      font-family: $ralewayRegular;
      font-size: 14px;
      color: $textColorWhite;
      word-wrap: break-word;
    }
  }

    //border: 1px solid white;

  
  
</style>