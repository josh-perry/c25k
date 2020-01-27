<template>
  <aside class="menu">
    <ul class="menu-list">
      <li v-for="w, index in weeks">
        <router-link
            :to="`/guide/${w}`"
            class="navbar-item"
            v-bind:class="{'is-active': index+1 == selectedWeek}">

          Week {{ w }}
        </router-link>
      </li>
    </ul>
  </aside>
</template>

<script>
import Data from '~/static/data.json'

export default {
  components: {
  },

  data() {
    return {
      selectedWeek: this.$route.params.week,
      weeks: []
    }
  },

  mounted() {
    this.weeks = [1, 2, 3, 4, 5, 6, 7, 8, 9];
  },

  methods: {
  }
}

</script>

<style scope>
.p {
  text-align: left;
}

.week {
  margin-top: 2%;
  margin-bottom: 2%;
}

.day {
  margin: 2%;
}

li {
  padding-left: 16px;
}

h2 {
  font-size: 1.6em;
}

h3 {
  font-size: 1.4em;
}
</style>
