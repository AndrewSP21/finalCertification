<template>
    <div>
        <BlogTop :topImg="require('@/assets/Project.png')" :title="'Our Project'" :text="'Home / Project'"
            :topTitle="'1'" />
        <ProjectSelector />
        <TheNumerator />
        <TheFooter />
    </div>
</template>
  
<script>
// @ is an alias to /src
import BlogTop from "../components/BlogTop.vue";
import ProjectSelector from "../components/ProjectSelector.vue";
import TheNumerator from "../components/Numerator.vue";
import TheFooter from "../components/TheFooter.vue";


export default {
    name: 'RProject',
    components: {
        BlogTop,
        ProjectSelector,
        TheNumerator,
        TheFooter,
    },

}
</script>
  
