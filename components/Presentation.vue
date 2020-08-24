<template>
  <div class= "mainPresentation">
    <h1>
      WE ARE IDLABS.
    </h1>
    <p>
    Grâce à notre approche rationalisée, nous nous assurons que nos clients construisent le <br>
    bon produit pour le marché approprié en déployant les meilleures stratégies digitales.
                                        
    </p>
    <h3>IDLABS, votre idée digitale sur mesure !</h3>
  
  

</div>
</template>
<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';

  .mainPresentation {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 100vh;
    background-image: url("../assets/image/idlabsWall.png");
    background-size: cover;
    background-repeat: no-repeat;
    padding: 0 16px;
    text-align: left;

    @include tablet-up {
        justify-content: center;
        padding: 0 0 0 8vw;
      }

    @include desktop-up {
        justify-content: center;
        padding: 0 0 0 20vw;
      }

    h1 {
      font-family: $poppinsBold;
      font-size: 50px;
      color: $textColorGreen;
      margin-bottom: 3vh;

       @include tablet-up {
        margin-bottom: 3vh;
        font-size: 80px;
      }

      @include desktop-up {
        margin-bottom: 3vh;
        font-size: 110px;
      }
    }
    p {
      color: white;
      margin-bottom: 6vh;

      @include tablet-up {
        margin-bottom: 6vh;
        font-size: 20px;
      }
    }
    h3 {
      font-family: $ralewayMedium;
      font-size: 20px;
      color: $textColorGreen;

      @include tablet-up {
        font-size: 30px;
      }
    }
    }
  
</style>