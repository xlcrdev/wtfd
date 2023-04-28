<template>
  <div class="grid grid-cols-3">
    <div class="post" v-for="post in posts" :key="post.id">
      
      <div class="p-4">
        <div class="max-w-sm rounded overflow-hidden shadow-lg mb-4">
          <img
            class="w-full"
            src="~assets/img/featured-default.jpg"
            alt="mountains"
          >
          <div class="px-6 py-4 pb-2 bg-gray-300">
            <div class="font-bold text-lg mb-2"><a :href="`blog/${post.slug}`" v-html="post.title.rendered"></a></div>
            <div class="text-xs text-green-500 mb2">{{ post.date }}</div>
            <div class="text-xs text-orange-500 mb2">{{ post.tags }}</div>
            <div class="text-white text-base">
            <div v-html="post.excerpt.rendered"></div>
              
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
  export default {
    computed: {
      posts() {
        return this.$store.state.posts;
      },
    },
    created() {
      this.$store.dispatch("getPosts");
    },
  };
</script>
