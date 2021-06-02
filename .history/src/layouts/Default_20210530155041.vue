<template>
  <div class="layout">
     <!-- Navigation -->
   
<!-- 默认插槽 -->
  <slot/>
  <!-- Footer -->
  <footer>
   
  </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>

</style>
