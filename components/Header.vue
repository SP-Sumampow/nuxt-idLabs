<template>
  <header class="header">
    <div class="header__barHeader barHeader">
      <p class= "barHeader__logo">IDLABS</p>
      <button @click="toggleMenu" class="barHeader__buttonMenu buttonMenu">
        <span class= "buttonMenu__bar"></span>
        <span class= "buttonMenu__bar"></span>
        <span class= "buttonMenu__bar"></span>
      </button>
    </div>
    <ul class="header__mainMenu" 
        :class="headerIsOpen ? 'isOpen' : 'isClose'">
      <li><nuxt-link to="/">ACCUEIL</nuxt-link></li>
      <li><a href="#services">SERVICES</a></li>
      <li><a href="#process">PROCESS</a></li>
      <li><nuxt-link to="/contact">CONTACT</nuxt-link></li>
    </ul>
  </header>
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
  .header {
    position: fixed;
    width: 100vw;
    top: 0;
    display: flex;
    //height: 10vh;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    background-color: black;

    @include tablet-up {
      height: 20vh;
      @include flexbox (column, space-around, center)
    }

    @include desktop-up {
        height: 10vh;
        @include flexbox (row, space-evenly, center);
        padding: auto 10vw;
      }


    &__barHeader {
      height: 8vh;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      width: 90%;

      @include tablet-up {
        width: auto;
        height: auto;
      }

      p {
        font-family: $ralewayMedium;
        font-size : 14px;
        letter-spacing : 5px;
        color : $textColorGreen;
        border-bottom: 1px solid white;
        line-height: 1.5;

        @include tablet-up {
          justify-self: center;
        }
      }

      .barHeader__buttonMenu {
        background-color: transparent;
        background-image: none;
        border: 1px solid transparent;
        width: 50px;
        height: 50px;
        padding: 1px 0;

        @include tablet-up {
          display: none;
        }


        .buttonMenu__bar {
          float: right;
          display: block;
          background-color: white;
          width: 30px;
          height: 2px;
          border-radius: 1px;
          margin-top: 4px;
        }
      }

    }
    &__mainMenu {
      width: 90%;
      list-style-type: none;
      color: white;
      font-family: $ralewayMedium;
      font-size: 13px;
      text-decoration: none;

      a {
          color: $textColorWhite;
          text-decoration: none;
        }

      li:hover {
          color: $textColorOnHover;
        }


      @include tablet-up {
        @include flexbox( row, space-around, center);

      }

      @include desktop-up {
        cursor: pointer;
        
      }

      &.isOpen {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        padding-top: 0;
        height: 25vh;
      }

      &.isClose {
        display: none;

      @include tablet-up {
          width: 50%;
          @include flexbox( row, space-around, center)        
      }

      @include desktop-up {
          width: 30%;
          @include flexbox( row, space-around, center)        
      }
      
      }
    }
  }
</style>