<template>
  <div class="thirdSection__progression">
    <BarProcess v-for="barProcess in barProcessList" :key="barProcess.id" :title=barProcess.title :percent=barProcess.percent :shouldBeDisplay=barProcessShouldBeDisplay />
  </div>
</template>

<script>
export default {
  props: {
    barProcessShouldBeDisplay: Boolean
  },
  data() {
    return {
      barProcessList: [
        {
          key: "1",
          title: "Brainstorming",
          percent: 20,
        },{
          key: "2",
          title: "Design Thinking & Prototype",
          percent: 15,
        },
        {
          key: "3",
          title: "Développement & Pré-Lancement",
          percent: 55,
        },
        {
          key: "4",
          title: "Lancement & Maintenance",
          percent: 10,
        }
      ]
    }
  },
  methods: {
    displayPercent: function () {
      this.barProcessList = this.barProcessList.map((barProcess) => {
        barProcess.shouldBeDisplay = true
        return barProcess
      })
    }
  }
}
</script>

<style lang="scss" scoped>
  @import '@/assets/sass/variables.scss';
  @import '@/assets/sass/typography.scss';
  
  .thirdSection__progression {
    width: 90vw;

    @include desktop-up {
        width: 40%;
    }
    //padding: 0 5vw;

  }
</style>
  