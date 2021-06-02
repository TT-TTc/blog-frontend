<template>
  <div >
    <header :class="['head',($route.name ||$route.path.includes('/post/') ) && 'sticky']">
      <div class="container">
        <div class="left">
          <g-link to="/">
            <Brand style="width: 60px;height: 24px;"></Brand>
          </g-link>
        </div>
        <nav class="right">
          <g-link to="/journal/" class="nav__link">
            Journal
          </g-link>
          <g-link to="/contact/" class="nav__link">
            Say Hi!
          </g-link>
        </nav>
      </div>
    </header>
    <!-- 默认插槽 -->
    <slot/>
    <!-- Footer -->
    <footer class="foot">
      <div class="container">
        Copyright © 2021
      </div>
    </footer>
  </div>
</template>

<script>
import Brand from '/static/svg/logo.svg'

export default {
  metaInfo: {
    title: '博客',
    meta: [
      {
        name: 'viewport',
        content: 'width=320,maximum-scale=1.3,user-scalable=no'
      }
    ]
  },
  components: {
    Brand
  },

}
</script>


<style scoped lang="scss">
.head.sticky{
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}
.head {
  z-index: 10;
  height: 6rem;

  .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 100%;
  }
}


.foot {
  font-size: .8rem;
  padding: 6rem 0;
}

.right {
  font-weight: bold;
  font-size: 14px;

  .nav__link {
    font-size: .9rem;
    font-weight: 600;
    text-decoration: none;
    margin-top: 4px;
    margin-right: 3rem;
    padding-bottom: 4px;
    border-bottom: 1px solid;
    border-color: transparent;
    transition: border .15s;
  }

  .nav__link:nth-of-type(1) {
    margin-right: 48px;
  }
  .nav__link:last-of-type{
    margin: 0;
  }

  .nav__link:hover {
    border-color: inherit;
  }
}
</style>
