<template>
    <div>
        <BlogTop :topImg="require('@/assets/Details.png')" :topTitle="''" />
        <ProjectDetails :items="getSomeArticles" />
        <TheFooter />
    </div>
</template>
  
<script>
// @ is an alias to /src
import BlogTop from "../components/BlogTop.vue";
import ProjectDetails from "../components/ProjectDetails.vue";
import TheFooter from "../components/TheFooter.vue";
import { mapMutations, mapActions, mapState, mapGetters } from "vuex";

export default {
    name: 'RProjectDetails',
    components: {
        BlogTop,
        ProjectDetails,
        TheFooter,
    },
    methods: {
        ...mapMutations(["SET_ARTICLES", "SET_SCOPE_PAGE", "SET_BLOGS"]),
    },
    computed: {
        ...mapActions(["fetchArticles", "fetchBlog"]),
        ...mapState(["articles", "fArticles"]),
        ...mapGetters(["getSomeArticles", "get3Articles"])
    },

}
</script>
  
