<template>
  <Layout>
    <div class="container">
      <div class="journal-hero">
        <h1 class="journal-header">
          a wise person once said...
        </h1>
      </div>
    </div>
    <g-link to="/" class="journal-post">
      <div class="container journal">
        <h2 class="journal-title">
          Gridsome with Forestry CMS
        </h2>
        <p class="journal-excerpt">
          Get up and running with Forestry CMS, a git-backed headless CMS with a slick editing interface.
        </p>
      </div>
    </g-link>
    <g-link to="/" class="journal-post">
      <div class="container journal">
        <h2 class="journal-title">
          VueJS for your next project
        </h2>
        <p class="journal-excerpt">
          Vue (pronounced /vjuː/, like view) is a progressive framework for building user interfaces.
        </p>
      </div>
    </g-link>
    <g-link to="/" class="journal-post">
      <div class="container journal">
        <h2 class="journal-title">
          macOS development environment
        </h2>
        <p class="journal-excerpt">
          Get up and running with a fresh macOS Catalina install
        </p>
      </div>
    </g-link>
    <g-link to="/" class="journal-post">
      <div class="container journal">
        <h2 class="journal-title">
          About Typography
        </h2>
        <p class="journal-excerpt">
          Font face, vertical rythm, readability, this long fake text should flow.
        </p>
      </div>
    </g-link>
  </Layout>

</template>

<script>
export default {
  name: 'journal'
}
</script>

<style scoped lang="scss">
.journal-hero {
  padding: 4rem 0;
  text-align: center;
  color: var(--color-base-1);

  .journal-header {
    font-size: 3rem;
    font-weight: 700;
    padding: 0;
    margin: 0;
  }
}

.journal-post {
  display: block;
  padding: 5rem 0;
  text-decoration: none;
  transition: background .5s ease;

  & > * {
    transition: transform .5s ease;
  }

  &:hover {
    background-color: var(--color-base-1);

    & > * {
      transform: translateX(4rem);

    }
  }


}



.journal-post:hover > {
  transform: translateX(4rem);
}

.container.journal {
  max-width: 720px;
}

.journal-title {
  font-size: 2rem;
  color: var(--color-contrast);
}
</style>
