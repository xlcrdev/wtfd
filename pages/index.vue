<template>
    <main>
      <div class="grid grid-cols-3">
        <div class="post" v-for="post in posts" :key="post.id">
          
          <div class="p-4">
            <div class="max-w-sm rounded overflow-hidden shadow-lg mb-4">
              <img
                class="w-full"
                src="~assets/img/featured-default.jpg"
                alt="mountains"
              >
              <div class="px-6 py-4 pb-2">
                <div class="font-bold text-xl mb-2"><a :href="`blog/${post.slug}`" v-html="post.title.rendered"></a></div>
                <div class="text-xs text-red-500 mb2">{{ post.date }}</div>
                <p class="text-gray-700 text-base">
                  <div v-html="post.excerpt.rendered"></div>
                  
                </p>
              </div>
            </div>
          </div>

        </div>
      </div>
    </main> 

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
