<template>
  <section class="secondSection__serviceCard">
    <ServiceCard  v-for="card in listOfCard" :key="card.id" :iconFontAwesome="card.iconFontAwesome" :title="card.title" :subTitle="card.subTitle"/>
  </section>
</template>

<script>
export default {
  data() {
    return {
      listOfCard: [
        {
          id: "1",
          iconFontAwesome: "cloud",
          title: "Application SASS",
          subTitle: "Appuyez-vous sur IDLABS expert pour concevoir vos applications web métier sur-mesure en mode SAAS."
        },
        {
          id: "2",
          iconFontAwesome: "mobile",
          title: "Application Mobile",
          subTitle: "Nous vous accompagnons et vous conseillons dans toutes les étapes de la création de votre application mobile."
        },
        {
          id: "3",
          iconFontAwesome: "archive",
          title: "API REST & GraphQL",
          subTitle: "De la stratégie à l’exécution, le succès d’une démarche orientée API demande une palette très diversifiée de savoir-faire."
        },
        {
          id: "4",
          iconFontAwesome: "building",
          title: "Microservice",
          subTitle: "L'approche Microservices est un style architectural qui structure l'application en plusieurs services faiblement couplés."
        },
        {
          id: "5",
          iconFontAwesome: "object-group",
          title: "Objets Connectés",
          subTitle: "Nous maîtrisons les technologies de l'IoT pour construire votre solution, standard ou sur mesure."
        },
        {
          id: "6",
          iconFontAwesome: "server",
          title: "Infrastructure",
          subTitle: "Nos experts assurent l'hébergement, l'infogérance et la mise en place de votre démarche DevOps."
        }
      ]
    }
  },
  methods: {
            toggleMenu: function () {
                this.headerIsOpen = !this.headerIsOpen
            }
        }
}
</script>

<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';
  
  .secondSection__serviceCard {
    width: 90vw;
    background-color: $primaryBackgroundColor;
    //padding: 0 5vw;

    @include tablet-up {
      width: auto;
        @include flexbox( row, space-around, center);
        display: flex;
        flex-wrap: wrap;
    }
  }
</style>