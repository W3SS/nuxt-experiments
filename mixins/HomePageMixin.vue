<template>
  <section class="container">
    <div>
      <app-logo/>
      <h1 class="title">
        {{ title }}
      </h1>
      <h2 class="subtitle">
        Nuxt.js project
      </h2>
      <ButtonLinks></ButtonLinks>
    </div>
    <router-view></router-view>
  </section>
</template>

<script>
import ButtonLinks from '~/components/ButtonLinks.vue';
import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo,
    ButtonLinks,
  },
  data() {
    return {
      title: 'HomePage',
    };
  },
};
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}


</style>
