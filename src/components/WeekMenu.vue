<template>
  <aside class="menu">
    <ul class="menu-list">
      <li>
        <router-link
            to="/guide"
            class="navbar-item">

          <span>
            Overview
          </span>

          <i class="fa fa-check"></i>
        </router-link>
      </li>

      <li v-for="w, index in weeks">
        <router-link
            :to="`/guide/${w}`"
            class="navbar-item"
            v-bind:class="{'is-active': index+1 == selectedWeek}">

          <span>
            Week {{ w }}
          </span>

          <i v-if="w <= 3" class="fa fa-check"></i>
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

i {
  float: right;
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
