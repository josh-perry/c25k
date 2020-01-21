<template>
  <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a class="navbar-item" href="/">
        <img src="http://placekitten.com/112/28" width="112" height="28">
      </a>

      <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navMenu">
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div class="navbar-menu" id="navMenu">
      <div class="navbar-start">
        <a class="navbar-item" href="/">
          What's C25k?
        </a>

        <router-link to="/guide" class="navbar-item">
          Guide
        </router-link>
      </div>
    </div>
  </nav>
</template>

<script>
import hamburger from '~/static/hamburger.js'
<script>

<style scoped>
</style>
