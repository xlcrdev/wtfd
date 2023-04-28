<template>
  <div class="grid grid-cols-1">
    <div class="bg-black">
      <nav>
        <app-nav></app-nav>
      </nav>
    </div>
    <div class="bg-gray-600">
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
