<template>
  <div class="guide">
    <div class="left">
      <WeekMenu/>
    </div>

    <div class="right">
      <GuideIndexText/>

      <Week
        v-if="selectedWeek"
        :week="selectedWeek"/>

    </div>
  </div>
</template>

<script>
import Data from '~/static/data.json'
import Week from '~/components/Week.vue'
import WeekMenu from '~/components/WeekMenu.vue'
import GuideIndexText from '~/components/GuideIndexText.vue'

export default {
  components: {
    Week,
    WeekMenu,
    GuideIndexText
  },

  data() {
    return {
      weeks: [],
      selectedWeek: null
    }
  },

  mounted() {
    this.fetchWeeks();
  },

  methods: {
    fetchWeeks: function(event) {
      Data.forEach((week, index) => {
        this.weeks.push({
          text: "Week " + (index + 1),
          done: false,
          days: week
        });
      });
    },

    weekClicked: function(week) {
      this.selectedWeek = week;
    }
  }
}
</script>

<style scoped>
.p {
  text-align: left;
}

.guide {
  display: flex;
}

.left {
  flex: 0 0 30%;
}

.right {
  flex: 1;
}
</style>
