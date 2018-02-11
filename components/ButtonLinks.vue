<template>
  <div class="links">
    <slot>
      <a
      href="https://nuxtjs.org/"
      target="_blank"
      class="button--green">Documentation</a>
      <a
      href="https://github.com/nuxt/nuxt.js"
      target="_blank"
      class="button--grey">GitHub</a>
    </slot>
  </div>
</template>

<style>
.links {
  padding-top: 15px;
}
</style>
