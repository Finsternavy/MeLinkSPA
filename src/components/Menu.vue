<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<style scoped>
.link {
  color: #d6662b;
}
</style>

<template>
  <nav
    id="Menu"
    class="menu uk-margin-left uk-margin-right uk-flex uk-flex-between uk-child-width-1-3 uk-padding"
  >
    <div class="left-nav">
      <div class="logo-container">
        <img src="" alt="LOGO" />
      </div>
    </div>
    <div class="right-nav uk-text-center">
      <div class="page-links-container uk-link uk-text-lead uk-text-background">
        <RouterLink class="uk-margin-right" to="/"
          ><span class="link">Home</span></RouterLink
        >
        <RouterLink to="/about"><span class="link">About</span></RouterLink>
      </div>
    </div>
    <div class="login-profile-container uk-text-right">
      <RouterLink to="/login"
        ><span class="link" uk-icon="icon: search"></span
      ></RouterLink>
    </div>
  </nav>
</template>
