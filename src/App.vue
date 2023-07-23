<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import Menu from "./components/Menu.vue";
</script>

<template>
  <div id="PrimaryLayout">
    <div id="MenuContainer" class="">
      <!-- FRN one way to pass franchise to components -->
      <Menu />
    </div>
    <section id="MainBodySection" class="uk-padding-remove">
      <div
        id="MainBodyContainer"
        class="mainbody container"
        uk-height-viewport="expand: false"
      >
        <RouterView />
      </div>
    </section>

    <section id="GlobalFooter" class="uk-section uk-margin-small uk-section-xsmall">
      <footer-navigation />
    </section>
  </div>
</template>

<style scoped></style>
