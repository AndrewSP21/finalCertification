<template>
    <div>
        <BlogTop :topImg="require('@/assets/Blog_details_Banner.png')" :topTitle="''" />
        <BlogDetails :blogArticles2="getBlogArticles20" :buttonTags="getTags" @filter="filter" />
        <TheFooter />
    </div>
</template>
  
<script>
// @ is an alias to /src
import BlogTop from "../components/BlogTop.vue";
import BlogDetails from "../components/BlogDetails.vue";
import { mapGetters, mapActions, mapMutations } from "vuex";
import TheFooter from "../components/TheFooter.vue";
// import { mapGetters, mapActions, mapMutations } from "vuex";


export default {
    name: 'RBLOGTop',
    components: {
        BlogTop,
        BlogDetails,
        TheFooter,

    },
    created() {
        this.fetchButtonTags0;
        this.fetchBlogArticles20;
    },
    computed: {
        ...mapActions(["fetchButtonTags0", "fetchBlogArticles20"]),
        ...mapGetters(["getTags", "getBlogArticles20"])
    },
    methods: {
        filter(id) {
            this.SET_FILTER_BLOG_ARTICLES0(id)
        },
        ...mapMutations(["SET_FILTER_BLOG_ARTICLES0"]),
    }
}
</script>
  
