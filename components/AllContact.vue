<template>
  <section class="contactinfo__allContact">
    <ContactInfo  v-for="contact in listOfContact" :key="contact.id" :iconFontAwesome="contact.iconFontAwesome" :titleContact="contact.titleContact" :detailContact="contact.detailContact"/>
  </section>
</template>

<script>
export default {
  data() {
    return {
      listOfContact: [
        {
          id: "1",
          iconFontAwesome: "map-marker",
          titleContact: "Adresse",
          detailContact: "88 Avenue du General de Gaulle, 92130 Issy-les-Moulineaux FRANCE"
        },
        {
          id: "2",
          iconFontAwesome: "mobile",
          titleContact: "Téléphone",
          detailContact: "+33 6 65 64 70 28"
        },
        {
          id: "3",
          iconFontAwesome: "envelope",
          titleContact: "Email",
          detailContact: "hello@idlabs.io"
        }
      ]
    }
  },
  asyncData() {
    return {
      listOfContact: [
        {
          id: "1",
          iconFontAwesome: "map-marker",
          titleContact: "Adresse",
          detailContact: "88 Avenue du General de Gaulle, 92130 Issy-les-Moulineaux FRANCE"
        },
        {
          id: "2",
          iconFontAwesome: "mobile",
          titleContact: "Téléphone",
          detailContact: "+33 6 65 64 70 28"
        },
        {
          id: "3",
          iconFontAwesome: "envelope",
          titleContact: "Email",
          detailContact: "hello@idlabs.io"
        }
      ]
    }
  },
  methods: {
        }
}
</script>

<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';
  
  .contactinfo__allContact {
    width: 90vw;
    background-color: $secondaryBackgroundColor;
    //padding: 0 5vw;

    @include tablet-up {
      width: auto;
        @include flexbox( row, space-between, center);
        display: flex;
        flex-wrap: wrap;
    }
  }
</style>