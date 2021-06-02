<template>
  <layout>
    <div class="project">
      <div class="container">
        <div class="project-header">
          <h1 class="project-title">
            {{ $page.posts.title }}
          </h1>
          <div class="project-info">
            <div class="categories-container">
              <div class="categories">
                <span class="label">Categories</span>
                <span class="category">
                  {{ $page.posts.categories }}
                </span>

              </div>
            </div>
            <div class="year-container">
              <span class="label">Year</span>
              <div>{{ $page.posts.year }}</div>
            </div>

          </div>
        </div>
        <div class="content">
          <p v-html="mdToHtml($page.posts.description)"></p>
          <p>
            <img class="g-image g-image--lazy g-image--loaded" :src="GRIDSOME_API_URL+$page.posts.image.url">
          </p>
        </div>
      </div>
    </div>
  </layout>
</template>
<page-query>
query ($id: ID!) {
posts: strapiPost(id: $id) {
id
title
categories
year
description
image{
url
}
}
}
</page-query>
<script>
import MarkdownIt from 'markdown-it'
const md = new MarkdownIt()
export default {
  data(){
    return{
    md,
    }
  },
  created() {
    console.log(this.$page)
  },
  methods: {
    mdToHtml(markdown){
      return md.render(markdown)
    }
  }
}
</script>

<style scoped lang="scss">
.project-header {
  padding: 20vh 0 4rem;
}

h1 {
  letter-spacing: -.01em;
}

.project-title {
  font-size: 4rem;
  margin: 0 0 4rem;
  padding: 0;
}

.project-info {
  display: flex;
  flex-wrap: wrap;
  font-size: .8rem;
}

.project-info > div {
  margin-right: 4rem;
}

.project-info > div:last-of-type {
  margin: 0;
}

img {
  max-width: 100%;
}

</style>
