<template>
  <div class="guide">
    <div class="buttons">
      <button
          class="button"
          v-for="w in weeks"
          v-bind:class="{'is-primary': w.done }"
          @click="weekClicked(w)">

        {{ w.text }}
      </button>
    </div>

    <Week
      v-if="selectedWeek"
      :week="selectedWeek"/>
  </div>
</template>

<script>
import Data from '~/static/data.json'
import Week from '~/components/Week.vue'

export default {
  components: {
    Week
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
	width: 60%;
	margin: 0 auto;
}
</style>
