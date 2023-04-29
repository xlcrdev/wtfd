<template>
  <div class="grid grid-cols-1">
    <div class="bg-gray-800">
      <nav>
        <app-nav></app-nav>
      </nav>
    </div>
    <div class="bg-gray-600">
      <nuxt />
    </div>
    <div class="p-3 bg-white font-mono text-xs italic text-right border-black">
      <p>hello world xlcrdev.com &copy; 2023</p>
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
  p {

  }

</style>
