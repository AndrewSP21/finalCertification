<template>
    <div>
        <MainPage />
        <ArticlesNews :articlesList="get3Articles" />
        <TheFooter />
    </div>
</template>
  
<script>
// @ is an alias to /src
import MainPage from "../components/MainPage.vue"
import ArticlesNews from "../components/ArticlesNews.vue";
import TheFooter from "../components/TheFooter.vue";
import { mapGetters, mapActions } from "vuex";


export default {
    name: 'RMainPage',
    components: {
        MainPage,
        ArticlesNews,
        TheFooter,
    },
    created() {
        this.fetchArticles;
    },
    computed: {
        ...mapActions(["fetchArticles"]),
        ...mapGetters(["get3Articles"])
    },
}
</script>
  
