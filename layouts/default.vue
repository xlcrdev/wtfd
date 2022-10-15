<template>
  <div class="grid grid-cols-1">
    <div class="">
      <nav>
        <app-nav></app-nav>
      </nav>
    </div>
    <div>XLCR Dev</div>
    <div>
      <nuxt />
    </div>
  </div>
</template>

<script>
import AppNav from "~/components/AppNav.vue";

export default {
  components: {
    AppNav
  }
};
</script>

<style>


</style>
