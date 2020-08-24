<template>
  <section v-waypoint="{ active: true, callback: logOne }" id="process" class="thirdSection">
    <div class= "thirdSection__titleSection titleSectionThree">
      <h2 class= "titleSectionThree__text">
        {{titleHeader}}
      </h2>
      <p class= "titleSectionThree__subText">
        {{subTitleHeader}}
      </p>
    </div>
    <AllProgression :barProcessShouldBeDisplay="barProcessShouldBeDisplay"/>
  </section>
</template>

<script>
export default {
  data() {
    return {
      titleHeader: "PROCESS",
      subTitleHeader: "Nous comprenons dès le départ que votre budget, votre temps et vos ressources peuvent être limités, nous vous proposons donc un modèle économique différent pour répondre à vos besoins spécifiques. Nous disposons de tous les outils et de tous les talents pour des lancements rapides et une livraison continue, offrant à votre entreprise une solution fluide, rapide, flexible et économique.",
      barProcessShouldBeDisplay: false
    }
  },
  methods: {
        logOne ({ el, going, direction }) {
          let elementId = el.id
          if (elementId === "process" && going === "in") {
            console.log(`${el.id} ${going} ${direction}`)
            this.barProcessShouldBeDisplay = true
          } else {
            this.barProcessShouldBeDisplay = false
          }
        }
      }
}
</script>



<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';
  
  .thirdSection {
    height: 100vh;
    max-width: 100vw;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: flex-start;
    background-color: $secondaryBackgroundColor;
    padding: 0 5vw;
    line-height: 1.5;

    @include desktop-up {
      height: 80vh;
      width: 90vw;
      @include flexbox(row, space-around, center);
      //padding: 10vw;
    }

    .titleSectionThree {
      line-height: 1.5;

      @include desktop-up {
        width: 40%;
      }

      &__text{
        font-family: $poppinsBold;
        font-size: 50px;
        color: $textColorGreen;
        line-height: 1.5;
        margin-bottom: 1vh;
      }

      &__subText{
        font-size: 18px;
        font-family: $ralewayRegular;
        color: $textColorWhite;
      }
    }

  }
</style>