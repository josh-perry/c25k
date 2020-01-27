<template>
  <div class="guide">
    <div class="left">
      <WeekMenu/>
    </div>

    <div class="right">
      <Week v-if="weekData" :week="weekData"/>
    </div>
  </div>
</template>

<script>
import Data from '~/static/data.json'
import Week from '~/components/Week.vue'
import WeekMenu from '~/components/WeekMenu.vue'

export default {
  components: {
    WeekMenu,
    Week
  },

  data() {
    return {
      week: this.$route.params.week,
      weekData: {}
    }
  },

  mounted() {
    this.weekData = {
      text: `Week ${this.week}`,
      days: [
        ["awda", "aaa"],
        ["aoda2", "a2dad2", "a2dad2"]
      ]
    }

    this.weekData.days = Data[this.week];
  }
}
</script>

<style scoped>
.guide {
	width: 60%;
	margin: 0 auto;
  display: flex;
}

.left {
  flex: 0 0 20%;
}

.right {
  flex: 1;
}
</style>
