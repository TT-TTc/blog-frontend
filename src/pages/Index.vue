<template>
  <Layout>
    <div class="container wrap">
      <div class="hero">
        <h1 class="title">Simplicity.Aesthetics. Value.</h1>
        <h2 class="subtitle">Hi there, I'm an independent Digital Designer & Art Director focused on digital design for
                             brands that like to have fun.</h2>
      </div>
      <div class="projects">
        <div class="project">
          <g-link to="/post/1">
            <img class="thumbnail" src="/img/xiangjiao.jpg" alt="">
            <h3 class="project-title">Banana</h3>
            <div class="categories">
              <span class="category">photography</span>
              <span class="category">pink</span>
            </div>
          </g-link>
        </div>
        <div class="project">
          <g-link to="/post/2">
            <img class="thumbnail" src="/img/菠萝.jpg" alt="">
            <h3 class="project-title">Pineapple</h3>
            <div class="categories">
              <span class="category">photography</span>
              <span class="category">blue</span>
            </div>
          </g-link>
        </div>
        <div class="project">
          <g-link to="/post/3">
            <img class="thumbnail" src="/img/冰淇淋.jpg" alt="">
            <h3 class="project-title">Pineapple</h3>
            <div class="categories">
              <span class="category">photography</span>
              <span class="category">blue</span>
            </div>
          </g-link>
        </div>
        <div class="project">
          <g-link to="/post/4">
            <img class="thumbnail" src="/img/胶卷.jpg" alt="">
            <h3 class="project-title">Porta400</h3>
            <div class="categories">
              <span class="category">photography</span>
              <span class="category">yellow</span>
            </div>
          </g-link>
        </div>
      </div>

    </div>
    <div>
      <div class="latest-journals-heading container">
        <span class="label">Latest and greatest</span>
      </div>
      <div class="latest-journals">
        <div class="container">
          <g-link to="/" class="journal">
            <h3 class="journal-title">Gridsome with Forestry CMS</h3>
          </g-link>
          <g-link to="/" class="journal">
            <h3 class="journal-title">VueJS for your next project</h3>
          </g-link>
          <g-link to="/" class="journal">
            <h3 class="journal-title">macOS development environment</h3>
          </g-link>
          <g-link to="/" class="journal">
            <h3 class="journal-title">About Typography</h3>
          </g-link>
        </div>
      </div>
    </div>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!',
  },
  name: 'HomePage'
}
</script>

<style scoped lang="scss">

.wrap{
  padding: 6rem 0 0;
}
.hero {
  text-align: center;
  width: 480px;
  max-width: 100%;
  margin: 0 auto;
  padding: 64px 0 128px;

  .title {
    font-size: 3rem;
    font-weight: bold;
    margin-bottom: 32px;
  }

  .subtitle {
    font-size: 19px;
    font-weight: 400;
    line-height: 30px;
    opacity: .6;
  }
}

.projects {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap: 4rem;

  .project {
    text-align: center;
    grid-column: auto/span 1;
  }

  .project:hover {
    .thumbnail {
      transform: scale(1.02);
      box-shadow: 0 20px 40px -20px rgba(0, 0, 0, 0.25);
    }
  }

  .project:nth-child(3n+1) {
    grid-column: auto/span 2;

  }

  .thumbnail {
    width: 100%;
    height: 560px;
    object-fit: cover;
    transition: all .15s ease;
    box-shadow: 0 0 40px -20px rgba(0, 0, 0, 0.25);
  }

  .project-title {
    font-size: 1rem;
    color: #000;
    margin: 2rem 0 1rem;
  }

  .categories {
    font-size: 0.8rem;
    color: #000;

    .category {
      margin-right: .8rem;

      &:last-of-type {
        margin: 0;
      }
    }

  }

}

.latest-journals-heading {
  margin-top: 6rem;
  margin-bottom: 1rem;
  font-size: .6rem;
  font-weight: 400;
  text-transform: uppercase;

  .label {
    display: block;
    font-weight: 700;
    margin-bottom: .5rem;
  }
}

.latest-journals {
  .container {
    display: flex;
    flex-wrap: wrap;
  }
}

.latest-journals {
  margin: 0;
  border-left: 0;
  border-right: 0;
  border-top: 1px solid var(--color-base-1);
  border-bottom: 1px solid var(--color-base-1);
}

.journal {
  flex: 0 0 25%;
  display: block;
  padding: 2rem;
  transition: background .25s ease;
  text-decoration: none;
  border-bottom: 1px solid var(--color-base-1);

  .journal-title {
    margin: 1em 0;
    font-size: 1rem;
    line-height: 1.35;
  }
}

.journal:first-child, .journal:nth-child(2), .journal:nth-child(3) {
  border: 0;
  border-right: 1px solid var(--color-base-1);
}

.journal:hover {
  background: var(--color-base-1);
}

.latest-journals {
  max-width: 100%;
  margin: 0 2rem;
  border: 1px solid var(--color-base-1);
}
</style>
