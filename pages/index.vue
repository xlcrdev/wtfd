<template>
  <div class="grid grid-cols-4">
    <div class="post" v-for="post in posts" :key="post.id">
      
      <div class="p-4">
        <div class="max-w-sm rounded shadow-lg mb-4">
          <img
            class=""
            :src="post.featured_image_src_large[0]"
            alt="" 
            height=""
          >
          <div class="px-6 py-4 pb-2 bg-gray-300">
            <div class="font-bold text-lg mb-2"><a :href="`blog/${post.slug}`" v-html="post.title.rendered"></a></div>
            <div class="text-xs text-green-500 mb2">{{ post.date }}</div>
            <div class="text-black text-base line-clamp-3>
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
