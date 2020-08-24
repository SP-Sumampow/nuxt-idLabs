<template>
  <footer class="footer">
    <h2 class="footer__logo footerLogo">
      <span class="footerLogo__id">ID</span>
      <span class="footerLogo__labs">LABS</span>
    </h2>
    <div class="footer__icons icons">
      <img class="icons__linkedin" src="/assets/icons/linkedin-in-brands.svg"/> 
      <i></i>
      <i></i>
    </div>
    <p class="footer__linkPage linkPage">
      <a class="linkPage__about"> À propos</a>
      -
      <a class="linkPage__mentionsLegale">Mentions Légales</a>
      -
      <a class="linkPage__politiqueConfidentialite">Politique de confidentialité</a>
    </p>
    <div class="footer__copyRight"></div>
    <p class="footer__message">
      Made with 
      <font-awesome-icon :icon="['fa', 'heart']"/>
      by idlabs
      </p>
  </footer>
  
</template>
<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';

  .footer {
    height: 60vh;
    width: 100vw;
    display: flex;
    flex-direction: column;
    justify-content: center;
    background-color: $primaryBackgroundColor;
    align-items: center;
    line-height: 1.5;


    &__logo {
      font-family: $poppinsRegular;
      letter-spacing: 3px;
      padding: 7px;
      border: 1px solid $textColorWhite;
      font-size: 30px;
      margin-bottom: 2px;

      .footerLogo__id {
        color: $textColorGreen;
      }

      .footerLogo__labs {
        color: $iconColor;
        margin-left: 0;
      }
    }

    &__icons {
      color: $textColorWhite;
      margin-bottom: 2px;

      .icons__linkedin {
        height: 10px;
        width: 10px;
        fill: $textColorWhite;
      }
    }

    &__linkPage {
      font-size: 16px;
      color: $textColorWhite;
      margin-bottom: 2px;
    }

    &__message {
      color: $textColorWhite;

      .fa-heart {
        color: $textColorGreen;
        height: 16px;
        width: 16px;
      }
    }

  }
  
</style>