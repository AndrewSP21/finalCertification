<template>
  <div class="yoyyo">
    <section class="articlesNews">
      <div class="arround">
        <div class="articlesNews__title">
          <router-link class="articlesNews__h1" to="/RBlog">Articles & News</router-link>
          <div class="articlesNews__h3">
            It is a long established fact that a reader will be distracted by
            the of readable content of a page when lookings at its layouts the
            points of using.
          </div>
        </div>
      </div>
      <div class="arround">
        <div class="articles">
          <article v-for="(i, id) in articlesList" :key="id" class="articleN">
            <div class="articleN_subcontent" v-bind:class="i.lighting">
              <router-link class="articlesNews__h1" to="/RBLOGTop">
                <img v-bind:src="i.src" alt="photo" class="articleN__img" />
              </router-link>

              <div class="articleN_data">
                <div class="articleN__text">{{ i.articleN__text }}</div>
                <div class="articleN_data_subcontainer">
                  <div class="articleN__date">{{ i.articleN__date }}</div>
                  <router-link class="articlesNews__h1" to="/RBLOGTop">
                    <svg class="articleN__button" xmlns="http://www.w3.org/2000/svg" width="52" height="53"
                      viewBox="0 0 52 53" fill="none">
                      <circle cx="26" cy="26.267" r="26" fill="#F4F0EC" />
                      <path d="M23.7714 32.9527L29.7143 26.267L23.7714 19.5813" stroke="#292F36" stroke-width="2"
                        stroke-linecap="round" stroke-linejoin="round" />
                    </svg>
                  </router-link>
                </div>
              </div>
              <router-link class="articlesNews__h1" to="/RBLOGTop">
                <div class="articleN__designName">{{ i.design }}</div>
              </router-link>
            </div>
          </article>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "ArticlesNews",
  props: ["articlesList"],

};
</script>

<style scoped lang="scss">
@import "../assets/style.css";
</style>
