<template>
  <div class="nav">
    <AppIcon></AppIcon>
    <ul class="flex">
      <li class="-mb-px mr-1">
        <a class="bg-gray inline-block border rounded py-2 px-4 text-blue-700 font-bold" href="/">Home</a>
      </li>
      <li class="mr-1">
        <a class="bg-gray inline-block border rounded py-2 px-4 text-blue-500 hover:text-white font-bold" href="/about">About</a>
      </li>
      <li class="mr-1">
        <a class="bg-gray inline-block border rounded py-2 px-4 text-blue-500 hover:text-white font-bold" href="/contact">Contact</a>
      </li>      
    </ul>
  </div>
</template>

<script>
import AppIcon from "@/components/AppIcon.vue";

export default {
  components: {
    AppIcon
  }
};
</script>

<style>
.nav {
  padding: 1em 100px;

  a {

    opacity: 0.8;
    &:hover {
      opacity: 1;
    }
  }
}

div {
  align-items: center;
  display: flex;
  height: 100%;
  width: 100%;
}

ul {
  padding-left: 0;

  li {
    display: inline-block;
    margin-right: 30px;
  }
}
</style>
