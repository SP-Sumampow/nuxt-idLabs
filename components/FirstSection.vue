<template>
  <section id="accueil" class="firstSection">
    <Header/>
    <Presentation/>
  </section>
</template>

<script>
export default {
  data() {
    return {
      headerIsOpen: false
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
  
  .firstSection {
    height: 100vh;
    width: 100vw;
    line-height: 1.5;
  }
</style>