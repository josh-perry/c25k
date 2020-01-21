<template>
  <div class="week">
    <h2>{{ week.text }}</h2>

    <div
        class="day"
        v-for="d, i in week.days">

      <h3>Day {{ i + 1 }}</h3>

      <ul>
        <li v-for="step in d">
          {{ step }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: ["week"]
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
